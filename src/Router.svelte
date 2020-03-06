<script>
  import { Router, Link, Route } from "svelte-routing";

  import Home from "./pages/Home.svelte";
  import PageNotFound from "./pages/PageNotFound.svelte";

  export let url = "";
</script>

<Router {url}>
  <div>
    <Route path="/" component={Home} />
    <Route component={PageNotFound} />
  </div>
</Router>
