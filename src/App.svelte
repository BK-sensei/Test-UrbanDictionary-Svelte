<script>
	//import { Router, Route, Link } from "svelte-routing";
	import { Router, Route } from "svelte-navigator";
	import Home from "./pages/Home.svelte";
	import Generator from "./pages/Generator.svelte";
	import Header from "./components/header.svelte"
	// export let url = ""; //This property is necessary declare to avoid ignore the Router --> utilisé avec svelte-routing
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

