<script>
	import Tailwindcss from './Tailwindcss.svelte';
	import Router from "svelte-spa-router";


	import Footer from "./components/footer.svelte";
	import Header from "./components/header.svelte";
	import Contact from './routes/contact.svelte';
	import Gallery from './routes/gallery.svelte';
	import Home from './routes/home.svelte';
	import Notfound from './routes/notfound.svelte';

	export let name;
</script>

<Tailwindcss />
<div class="flex flex-col h-screen">


<Header/>

<main>

<Router routes = {{
	"/":Home,
	"/contact":Contact,
	"/gallery":Gallery,
	"*":Notfound,
}}
/>

</main>

<Footer/>

</div>
<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

