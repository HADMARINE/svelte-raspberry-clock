<script>
  import moment from "moment";
  import { Button } from "sveltestrap";

  let timenow;
  let isVisible = true;

  setInterval(() => {
    timenow = moment().format("LTS");
  }, 100);

  function toggleOnOff() {
    isVisible = !isVisible;
  }
</script>

<style lang="scss">
  .wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    width: 100vw;
    background-color: rgb(24, 24, 24);
    font-size: 200px;
    font-weight: 500;
    color: white;
    overflow: hidden;
    @media screen and (max-width: 1200px) {
      font-size: 150px;
    }
    @media screen and (max-width: 800px) {
      font-size: 100px;
    }
  }

  .floatViewPort {
    position: absolute;
    bottom: 30px;
    display: flex;
    justify-content: center;
    width: 100vw;
  }

  .invisible {
    color: black;
    background-color: black;
    height: 100vh;
    width: 100vw;
  }
</style>

<svelte:head>
  <link
    rel="stylesheet"
    href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" />
</svelte:head>
<div class={isVisible ? 'wrapper' : 'invisible'}>
  <p>{timenow}</p>

</div>

<div class="floatViewPort">
  <Button on:click={toggleOnOff}>{isVisible ? 'OFF' : 'ON'}</Button>
</div>
