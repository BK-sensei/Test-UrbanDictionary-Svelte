<script>
	//import { Router, Route, Link } from "svelte-routing";
	import { Router, Route } from "svelte-navigator";
	import Home from "./pages/Home.svelte";
	import Generator from "./pages/Generator.svelte";
	//import About from "./pages/About.svelte";
	//export let url = ""; //This property is necessary declare to avoid ignore the Router
  </script>

<header>

    <h1>Random Definition Generator</h1>

    <h2>from Urban Dictionary</h2>

</header>
<Router>
	<Route path="/">
		<Home />
	</Route>
	<Route path="/generator">
		<Generator />
	</Route>
	
</Router>


<!-- 
<Router url="{url}">
	<div>
	   <Route path="/"><Home /></Route>
	</div>
</Router> -->

<style>
	 
	* {
	  margin: 0;
	  padding: 0;
	  box-sizing: border-box;
	}
	
	header {
	  width: 100%;
	  background-color: black;
	  display: flex;
	  flex-direction: column;
	  align-items: center;
	  text-align: center;
	  font-family: Lora;
	  font-style: normal;
	  font-weight: bold;
	  padding: 20px 0px;
	}
	
	h1 {
	  font-size: 48px;
	  line-height: 61px;
	  text-align: center;
	  color: #FFFFFF;
	}
	
	h2{
	  font-size: 24px;
	  line-height: 31px;
	  color: #EFFF00;
	}
	
	</style>