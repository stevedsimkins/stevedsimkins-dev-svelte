<script:head>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;800&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Mulish:wght@400;500&display=swap');
  </style>
</script:head>

<script>
  import Landing from "../components/Landing.svelte"
  import MenuButton from "../components/MenuButton.svelte"
  import Menu from "../components/Menu.svelte"
  import { fly } from "svelte/transition"
  
  let menuOpen = false 
</script>

<Landing />
<MenuButton bind:menuOpen={menuOpen} />
{#if menuOpen}
  <Menu />
{/if}
<style>

  :global(*) {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: 'Playfair Display', serif;
  }

</style>
