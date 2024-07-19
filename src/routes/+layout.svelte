<script>
  import Navigation from '$lib/Navigation.svelte';
  import Footer from '$lib/Footer.svelte';
  import '../app.css';
</script>

<body>
  <Navigation />
  <slot />
  <Footer {Footer} />
</body>