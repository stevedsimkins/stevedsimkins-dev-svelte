<script>
  import { slide } from "svelte/transition"
</script>

<div transition:slide="{{delay: 250, duration: 500}}" class="container">
  <div class="menu-copy">
    <a class="link" data-content="Blog" target="_blank" href="https://medium.com/@stevedsimkins">Blog</a>
    <a class="link" data-content="Twitter" target="_blank" href="https://twitter.com/stevedsimkins">Twitter</a>
    <a class="link" data-content="Github" target="_blank" href="https://github.com/stevedsimkins">Github</a>
    <a class="link" data-content="Contact" target="_blank" href="mailto:stevedsimkins@gmail.com">Contact</a>
  </div>
</div>

<style>
.container {
  height: 100vh;
  width: 100%;
  background: white;
  z-index: 2;
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  }
  .menu-copy {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    width: 90%;
  }
  a {
    font-size: 90px;
    color: black;
    text-decoration: none;
    position: relative;
    display: inline-block;
    overflow: hidden;
  }
  a:before {
    position: absolute;
    content: attr(data-content);
    background: linear-gradient(45deg, #ab66ff, #81ecff);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    color: transparent;
    clip-path: polygon(0 0, 0 0, 0% 100%, 0% 100%);
    transition: clip-path 0.5s ease;
  

  }
a:hover::before {
  clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
}

</style>
