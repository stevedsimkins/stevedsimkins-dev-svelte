<script:head>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;800&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Mulish:wght@400;500&display=swap');
  </style>
  <title>Steve Simkins</title>
  <meta
    name="description"
    content="Community Manager, Web3 Developer, Technical Writer"/>

  <meta property="og:type" content="website">
  <meta property="og:url" content="https://www.stevedsimkins.dev/">
  <meta property="og:title" content="Steve Simkins">
  <meta property="og:description" content="Community Manager, Web3 Developer, Technical Writer">
  <meta property="og:image" content="https://stevedsimkins.mypinata.cloud/ipfs/QmXVuzKtgt4tS8KCbRVAqdRXVMCJybNUP3BgFQcWsefKtH">
  
  <!-- Twitter -->
  <meta name="twitter:card" content="summary" />
  <meta name="twitter:site" content="@stevedsimkins" />
  <meta name="twitter:creator" content="@stevedsimkins" />
  <meta property="og:url" content="https://www.stevedsimkins.dev/" />
  <meta property="og:title" content="Steve Simkins" />
  <meta property="og:description" content="Community Manager, Web3 Developer, Technical Writer" />
  <meta property="og:image" content="https://stevedsimkins.mypinata.cloud/ipfs/QmXVuzKtgt4tS8KCbRVAqdRXVMCJybNUP3BgFQcWsefKtH" />

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
