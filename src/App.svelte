<script>
	import { Router, Route } from 'svelte-navigator';
	import Header from './components/header.svelte';
	import Home from './routes/Home.svelte';
	import Generator from './routes/Generator.svelte';
</script>

<Header />
<Router>
	<Route path="/">
		<Home />
	</Route>
	<Route path="/generator">
		<Generator />
	</Route>
</Router>






