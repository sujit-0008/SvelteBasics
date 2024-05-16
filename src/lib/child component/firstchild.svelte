<script>
  import { createEventDispatcher } from "svelte";
  export let msg;
  const dispatch = createEventDispatcher();
  const SendEvent = () => {
    dispatch("customEvent", `massage for Parent `);
  };
</script>

<main>
  <div>
    <p>This is child Component</p>
    <p>{msg}</p>
    <button on:click={SendEvent}>Send msg to parent </button>
  </div>
</main>

<style>
</style>
