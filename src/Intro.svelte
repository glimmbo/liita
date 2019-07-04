<script>
  import Title from "./TitleVid.svelte";
</script>

<style>
  #container {
    background-color: transparent;
    position: relative;
  }

  #slogan {
    bottom: 2%;
    left: 0%;
    right: 0%;
    display: flex;
    justify-content: center;
    position: absolute;
  }

  h2 {
    animation: slideUp 3s 8s forwards;
    color: var(--pink);
    font-family: "Mr Dafoe";
    font-size: 2em;
    margin: 0;
    opacity: 0;
    padding-bottom: 2em;
    text-align: center;
    text-decoration: underline;
    z-index: 2;
  }

  @keyframes slideUp {
    from {
      transform: translateY(10vh);
    }
    to {
      opacity: 1;
    }
  }
</style>

<div id="container">
  <Title />
  <div id="slogan">
    <h2>Let your love take flight</h2>
  </div>
</div>
