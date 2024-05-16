<script>
  import Hero from "../lib/hero.svelte";
  import Firstchild from "../lib/child component/firstchild.svelte";
  let childMsg;
  const HandleEvent = (event) => {
    childMsg = event.detail;
  };
</script>

<main>
  <Hero msg="Sending Props + Event dispatch" />
  <p>This is Parent component</p>
  <p>msg from child {childMsg}</p>
  <Firstchild msg="MSG from parent" on:customEvent={HandleEvent} />
</main>

<style>
</style>
