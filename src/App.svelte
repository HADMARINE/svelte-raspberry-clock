<script>
  import { Router, Link, Route } from "svelte-routing";
  import PageNotFound from "./pages/PageNotFound.svelte";

  export let url = "";
</script>

<style>
  :global(body) {
    margin: 0;
    padding: 0;
  }
</style>

<Router {url}>
  <div>
    <Route component={PageNotFound} />
  </div>
</Router>
