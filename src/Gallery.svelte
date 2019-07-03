<script>

</script>

<style>
  #container {
    background-color: var(--darkteal);
    height: 100%;
    display: grid;
    grid-template-columns: repeat(2, 50vw);
    grid-template-rows: repeat(4, 25vh);
    position: relative;
  }
  img {
    display: block;
    height: 100%;
    width: 100%;
  }


  /* try: on click, fills section. on click again, or scroll away, return to slot */
  img:active {
    position: absolute;
    height: 100vh;
    width: 100vw;
    z-index: 2;
  }
</style>

<!-- https://codepen.io/tutsplus/pen/rQrVBg -->

<div id="container">
  <img src="heart.png" alt="">
  <img src="heart.png" alt="">
  <img src="heart.png" alt="">
  <img src="heart.png" alt="">
  <img src="heart.png" alt="">
  <img src="heart.png" alt="">
  <img src="heart.png" alt="">
  <img src="heart.png" alt="">
</div>
