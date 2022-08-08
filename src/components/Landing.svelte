<script>
  import LandingCopy from "./LandingCopy.svelte"
</script>

<div class="container">
  <LandingCopy />
</div>

<style>
  .container {
    height: 100vh;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  @media screen and (max-width: 750px){
    .container {
      width: 90%;
      margin: 0 auto;
    }
  }
</style>
