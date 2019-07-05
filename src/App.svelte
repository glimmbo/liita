<script>
	import Intro from "./Intro.svelte"
	import Description from "./Description.svelte"
	import Gallery from "./Gallery.svelte"
	import Contact from "./Contact.svelte"
</script>

<style>
/* moved to global.css */
	section {
		box-sizing: border-box;
		height: 100vh;
		width: 100vw;
		scroll-snap-align: start;
	}
</style>

<section id="intro">
	<Intro/>
</section>

<section id="description">
	<Description/>
</section>

<section id="gallery">
	<Gallery/>
</section>

<section id="contact">
	<Contact/>
</section>
