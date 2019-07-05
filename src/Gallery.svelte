<script>
  // import pics from "pics.json"?
  import Modal from "./ImageModal.svelte";

  let modal = {};
  let showModal = false;

  const showModalPic = e => {
    e.preventDefault();
    modal.src = e.currentTarget.style.backgroundImage.slice(5,-2);
    showModal = true;
  };

  const clearModal = e => {
    e.preventDefault();
    showModal = false;
    modal = {};
  };
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

  #modalImg {
    height: 100%;
    width: 100%;
  }

  @media (min-width: 500px) {
    #container {
      background-color: var(--darkteal);
      height: 100%;
      display: grid;
      grid-template-columns: repeat(4, 25vw);
      grid-template-rows: repeat(2, 50vh);
      position: relative;
    }
  }
</style>

<div id="container">
  <div class="thumbnail" style="background:url('images/cliff.png') center/cover no-repeat" on:click={showModalPic}></div>
  <div class="thumbnail" style="background:url('images/cliffKiss.png') center/cover no-repeat" on:click={showModalPic}></div>
  <div class="thumbnail" style="background:url('images/crowd.png') center center / cover no-repeat" on:click={showModalPic}></div>
  <div class="thumbnail" style="background:url('images/dance.png') center center / cover no-repeat" on:click={showModalPic}></div>
  <div class="thumbnail" style="background:url('images/dock.png') center center / cover no-repeat" on:click={showModalPic}></div>
  <div class="thumbnail" style="background:url('images/beach.png') center center / cover no-repeat" on:click={showModalPic}></div>
  <div class="thumbnail" style="background:url('images/dockAbove.png') right / cover no-repeat" on:click={showModalPic}></div>
  <div class="thumbnail" style="background:url('images/jump.png') 55% 50%/400% no-repeat" on:click={showModalPic}></div>

  {#if showModal}
    <Modal on:close={clearModal}>
      <div id="modalImg" style="background:url({modal.src}) {modal.src === "images/dockAbove.png" ? "right" : "center"} center / cover no-repeat">
      </div>
    </Modal>
  {/if}
</div>
