<script>
  // import pics from "pics.json"?
  import Modal from "./ImageModal.svelte";

  let modal = {};
  let showModal = false;

  const showModalPic = e => {
    e.preventDefault();
    modal.src = e.currentTarget.src
    modal.alt = e.currentTarget.alt
    showModal = true;
  };

  const clearModal = e => {
    e.preventDefault();
    showModal = false;
    modal = {};
  }
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
</style>

<div id="container">
  <!-- {#each pics as pic}
    <img src="{pic.src}" alt="{pic.description}">
  {/each} -->
  <img src="heart.png" alt="" on:click={showModalPic} />
  <img src="ig.svg" alt="" on:click={showModalPic} />
  <img src="heart.png" alt="" on:click={showModalPic} />
  <img src="heart.png" alt="" on:click={showModalPic} />
  <img src="heart.png" alt="" on:click={showModalPic} />
  <img src="heart.png" alt="" on:click={showModalPic} />
  <img src="heart.png" alt="" on:click={showModalPic} />
  <img src="heart.png" alt="" on:click={showModalPic} />

  {#if showModal}
    <Modal on:close={clearModal}>
      <img src="{modal.src}" alt="{modal.alt}" />
    </Modal>
  {/if}
</div>
