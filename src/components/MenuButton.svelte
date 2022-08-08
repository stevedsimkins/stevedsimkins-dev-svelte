<script>
  
  export let menuOpen = false;

  function toggleMenu() {
    menuOpen = !menuOpen
    console.log(menuOpen)
  }

  export let ariaLabel = 'toggleMenu' 
  export let width = 100

</script>

<div class="circle" on:click={toggleMenu}>
    <svg
    class:menuOpen
    viewBox="0 0 100 100"
    fill="none"
    stroke="#ab66ff"
    stroke-width="4"
    {width}
  >
    <path
      class="top"
      d="m 30,33 h 40 c 3.722839,0 7.5,3.126468 7.5,8.578427 0,5.451959 -2.727029,8.421573 -7.5,8.421573 h -20"
    />
      <path class="middle" d="m 30,50 h 40" />
    <path
      class="bottom"
      d="m 70,67 h -40 c 0,0 -7.5,-0.802118 -7.5,-8.365747 0,-7.563629 7.5,-8.634253 7.5,-8.634253 h 20"
    />
    </svg>
</div>

<style>

  .circle {
    width: 100px;
    height: 100px;
    border: 4px solid black;
    border-radius: 50%;
    position: absolute;
    right: 10%;
    bottom: 10%;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 3;
    cursor: pointer;
  }

  :root {
      --transition-duration: 400ms;
    }

  button {
    cursor: pointer;
    display: flex;
    align-items: center;
    overflow: hidden;
  }

  svg {
    transition: transform var(--transition-duration);
  }

  .top {
    stroke-dasharray: 40 160;
    transition: stroke-dashoffset var(--transition-duration);
  }

  .middle {
    transform-origin: 50%;
    transition: transform var(--transition-duration);
  }

  .bottom {
    stroke-dasharray: 40 85;
    transition: stroke-dashoffset var(--transition-duration);
  }

  .menuOpen {
    transform: rotate(45deg);
  }

  .menuOpen .top,
.menuOpen .bottom {
    stroke-dashoffset: -64px;
  }

  .menuOpen .middle {
    transform: rotate(90deg);
  }

  @media screen and (max-width: 750px){
    .circle {
      bottom: 5%;
    }
  }

</style>
