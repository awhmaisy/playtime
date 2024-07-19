<script>
	let items = [
		{
			title: 'day 001',
			date: '05.05.2024',
			image: 'images/funnyland/zappy teevee.jpg',
			description: `day one
it's may fifth! yay.

today i woke up as late as i possibly could,
started cleaning,
got in a very heated conversation,
cleaned some more.
today is the first day that i'm free from university duties, so i'm taking some time to tidy. i have so many papers EVERYWHERE, at some point i think i give up on being analog.

next, i've got to clean
1. the rest of my file folders
2. my vanity and its horrendous drawer
3. the clothing drawers
4. my closet, and take out all of the unnecessary jackets
5. fold and tuck away my plain shirts
6. the bins of high school clothing downstairs
7. once that's all done, i really want to clean out my computer files!!! she's so slow for NO reason. bruh.

so yes! it's a day of cleaning, trying to feel clean, and trying to calm my mind. i'm going way fast!

also, although i love paper, i think i will make a new cycle

gather
- read online
- learn to annotate from a screen
- wear the damn blue light glasses bro
- take notes for EVERYTHING in ONE notebook. none of this 'notebook per subject' bullshit
- consolidate the date-dependent books.
- abide by state-dependent books and papers.
- enjoy it

today i have new questions. i wonder
- what is the proper way to organize mac files? does adding things to my downloads versus my desktop versus a mysterious and unknown location alter the impact of the file size?
- what do all of these words in terminal mean
- why is my computer SO DAMN SLOW
- how do i fix my computer help`
		},
		{
			title: 'day 002',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/yunstudio.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 003',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/write on him, write with him.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 004',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/we are not meant to be discarded.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 005',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/tie me with a bow.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 006',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/things should be protected.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 007',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/some thoughts (are worthwhile).jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 008',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/sobbing at work.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 009',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/snow garden.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 010',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/see me clearly by hernan ardila.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 011',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/put her on display, if you love her.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 012',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/open the windows.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 013',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/mostly you can be saved.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 014',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/miracles are created.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 015',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/middleground.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 016',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/look for me on tracing paper.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 017',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/heart of air and clouds and birds.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 018',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/fish once swam.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 019',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/everybunny comes from somewhere.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 020',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/do for love.jpg',
			description: 'soon, you may see'
		},
        {
			title: 'day 021',
			type: 'parsing and collecting',
			date: '05/05/2024',
			image: 'images/funnyland/beginner\'s spirit.jpg',
			description: 'soon, you may see'
		},
	];

	let selectedItem = null;

	function selectItem(item) {
		selectedItem = item;
	}

	function renderDescription(description) {
		return marked(description);
	}
</script>

<!-- ... existing code ... -->
<h1>land here... hopefully safe!</h1>
<p>
	this site is made with the <em>director</em> typeface from ange degheest, as an homage to
	typewriter models. the typeface was specifically created to reflect the 'prestige and authority'
	of the Hermes typewriter models. though constricting, degheest crafted a contrasting design.. with
	gentle serifs and pleasant terminals. this site is made by mei (#justforfun) and i do hope you
	find pleasure here, very soon / my twitter <a href="https://twitter.com/awhmaisy">@awhmaisy</a>
	<br />
	<br />
	<br />
	unfortunately, you will not enjoy this if you are on a mobile device. do not do that.
</p>

<div class="container">
	<div class="left-side">
		{#each items as item}
			<div class="item" on:click={() => selectItem(item)}>
				{item.title} - {item.date}
			</div>
		{/each}
	</div>
	<div class="right-side">
		{#if selectedItem}
			<img src={selectedItem.image} alt={selectedItem.title} style="width: 100%;" />
			<p class="description">{selectedItem.description}</p>
		{/if}
	</div>
</div>

<style>
	p {
		font-size: 12px;
		text-align: justify;
	}

	a {
		text-decoration: none;
		color: #ff6bfd;
		animation: blink 1s infinite;
	}

	@keyframes blink {
		0%,
		100% {
			opacity: 1;
		}
		50% {
			opacity: 0;
		}
	}

	.container {
		display: flex;
	}

	.left-side,
	.right-side {
		flex: 1;
		padding: 10px;
	}

	.left-side {
	}

	.item {
		cursor: pointer;
		margin-bottom: 10px;
	}

	.description {
		margin-top: 10px;
		white-space: pre-wrap; /* Preserve line breaks */
	}
</style>
