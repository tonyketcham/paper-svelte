<script>
  export let resize = true;

  import { paper } from "paper";
  import newPaperCanvas from "./paperCanvas.js";
  import { onMount } from "svelte";
</script>

<style>
  /* Scale canvas with resize attribute to full size */
  canvas[resize] {
    width: 100%;
    height: 100%;
  }
</style>

{#if !resize}
  <canvas use:newPaperCanvas />
{:else}
  <canvas use:newPaperCanvas resize />
{/if}
