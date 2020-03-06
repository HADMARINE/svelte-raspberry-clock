<script>
  import Router from "./Router.svelte";
  export let url = "";
</script>

<style>
  @import url(//spoqa.github.io/spoqa-han-sans/css/SpoqaHanSans-kr.css);
  @import url(//spoqa.github.io/spoqa-han-sans/css/SpoqaHanSans-jp.css);
  @import url("https://fonts.googleapis.com/css?family=Noto+Sans&display=swap");

  :global(*) {
    font-family: "Spoqa Han Sans", "Spoqa Han Sans JP", "Sans-serif",
      "Noto Sans", serif;
    margin: 0;
  }

  :global(body) {
    background-color: rgb(24, 24, 24) !important;
  }
</style>

<svelte:head>
  <link
    rel="stylesheet"
    href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" />
</svelte:head>

<Router {url} />
