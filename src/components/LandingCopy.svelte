<script>

import { onMount } from "svelte"

const texts = ['Community Manager', 'Technical Writer', 'Web3 Developer', 'Content Creator']
let count = 0
let index = 0
let currentText = ''
let letter = ''
let typingFill

function type() {
 
  if(count === texts.length){
    count = 0;
  }
  currentText = texts[count]
  letter = currentText.slice(0, ++index)

  typingFill = letter

  if(letter.length === currentText.length){
    count ++
    index = 0
    setTimeout(type, 1500)
  } else {
    setTimeout(type, 100)
  }
  
}

onMount(type())

</script>

<div class="copy-container">
    <h2>Hey there!</h2>
    <h1 class="large-text">I’m Steve</h1>
    <h2 class="typing">{typingFill}</h2>
</div>

<style>
  h2 {
    font-size: 50px;
  }
  .large-text {
    font-size: 283px;
  }
  .typing {
    font-family: 'Mulish', sans-serif;
    background: -webkit-linear-gradient(45deg, #ab66ff, #81ecff, #16f195);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    color: transparent;
  }
  .typing::after {
    content: "";
    width: 5px;
    height: 5%;
    margin-left: 5px;
    border-right: 5px solid #ab66ff;
    animation: blink 0.7s infinite ease-out;
  }

  @keyframes blink {
    0% {
      opacity: 0;
    }
    50% {
      opacity: 1;
    }
    100% {
      opacity: 0;
    }
  }

  @media screen and (max-width: 1200px){
    .large-text {
      font-size: 160px;
    }
    h2 {
      font-size: 38px;
    }
    .typing {
      font-size: 50px;
    }
  }

  @media screen and (max-width: 430px){
    .large-text {
      font-size: 120px;
    }
    h2 {
      font-size: 28px;
    }
    .typing {
      font-size: 28px;
    }
  }

</style>
