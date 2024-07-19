<script>
	import { page } from '$app/stores';

	import { onMount } from 'svelte';

	let isPlaying = false;
	let audio;

	function togglePlayPause() {
		if (isPlaying) {
			audio.pause();
		} else {
			audio.play();
		}
	}

	function skip() {
		audio.currentTime += 10; // Skip forward 10 seconds
	}

	function restart() {
		audio.currentTime = 0; // Restart the track
		if (!isPlaying) {
			audio.play();
		}
	}

	onMount(() => {
		audio = document.getElementById('audio');
		audio.onplay = () => (isPlaying = true);
		audio.onpause = () => (isPlaying = false);
	});
</script>

<!--start of nav bar! hiiie ₊˚꒰ა ♡ ໒꒱︰-->
<nav>
	<a href="/">come home</a>
	<a href="/hear me">hear me</a>
	<a href="/adopt me">adopt me</a>
	<a href="/read me">read me</a>
	<div class="music-player">
		<div class="tooltip">
			<img src="/images/album-cover.jpeg" alt="GAMES by Games, Album Cover" class="album-cover" />
			<span class="tooltiptext">GAMES by games, produced by INDEX:records in UK</span>
		</div>
		{#if isPlaying}
			<button class="play-button" on:click={togglePlayPause}>paws</button>
		{:else}
			<button class="play-button" on:click={togglePlayPause}>play (with me)</button>
		{/if}
		<button class="skip-button" on:click={skip}>skip</button>
		<button class="restart-button" on:click={restart}>re:start</button>
		<audio id="audio" src="/music/song.mp3"></audio>
	</div>
</nav>

<style>
	nav {
		display: flex;
		justify-content: space-between;
		align-items: justify;
		margin: 0;
		width: 100%;
		padding: 0;
		box-sizing: border-box;
		font-size: 12px;
	}

	nav a {
		flex-grow: 0;
		text-align: center;
		text-decoration: none;
		color: inherit;
		padding: 0 0px;
	}

	nav a:hover {
		color: #ff6bfd;
	}

	.music-player {
		display: flex;
		align-items: center;
	}

	.tooltip {
		position: relative;
		display: inline-block;
	}

	.tooltip .tooltiptext {
		visibility: hidden;
		width: 120px;
		background-color: rgba(0, 0, 0, 0.5);
		color: #fff;
		text-align: center;
		border-radius: 6px;
		padding: 5px;
		position: absolute;
		z-index: 1;
		top: 125%;
		left: 50%;
		margin-left: -60px;
		opacity: 0;
		transition: opacity 0.3s;
	}

	.tooltip:hover .tooltiptext {
		visibility: visible;
		opacity: 1;
	}

	.album-cover {
		width: 40px;
		height: 40px;
		margin-right: 10px;
	}

	.play-button,
	.skip-button,
	.restart-button {
		font-family: 'Director Regular', serif;
		font-size: 12px;
		background-color: transparent;
		border: none;
		cursor: pointer;
		color: inherit;
	}
</style>
