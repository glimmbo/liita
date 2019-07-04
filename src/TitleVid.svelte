<script>
</script>
<style>
  #container {
    position: relative;
  }

  video {
    object-fit: cover;
    width: 100%;
    height: 100vh;
  }
  pre {
    color: red;
    padding: 1em;
    position: absolute;
    top: 0%;
  }

  @keyframes fadeIn {
    from {
      fill: rgba(250, 247, 250, 0);
    }
    to {
      fill: rgba(250, 247, 250, .9);
    }
  }

  svg {
    width: 100%;
    height: 100%;
    position: absolute;
  }
  svg text {
    text-anchor: middle;
  }
  #love, #air {
    font-family: 'Mr Dafoe';
    font-size: 20em;
  }
  #isinthe {
    font-family: 'Montserrat';
    font-weight: 700;
    font-size: 3em;
  }
  svg mask rect {
    animation: fadeIn 4s 7s forwards;
    /* fill: rgba(250, 247, 250, 1); */
  }
  svg > rect {
    fill: var(--white);
    -webkit-mask: url(#mask);
    mask: url(#mask);
  }
</style>

<div id="container">
  <svg
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 1920 1080"
    width="1920px"
    height="1080px"
    preserveAspectRatio="xMidYMid slice">
    <defs>
      <mask id="mask" x="0" y="0" width="1920" height="1080">
        <rect x="0" y="0" width="100%" height="100%" />
        <text id="love" x="50%" y="30%">Love</text>
        <text id="isinthe" x="50%" y="50%">is in the</text>
        <text id="air" x="50%" y="80%">Air</text>
      </mask>
    </defs>
    <rect x="0" y="0" width="1920" height="1080" />
  </svg>

  <video loop muted autoplay playsinline id="video" />
  <pre />
</div>
