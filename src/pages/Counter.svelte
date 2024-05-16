<script>
  import Hero from "../lib/hero.svelte";

  let count = 0;
  const increment = () => {
    count += 1;
  };
  const decrement = () => {
    if (count > 0) {
      count -= 1;
    }
  };
</script>

<main>
  <Hero msg="This is Counter" />
  <div><button on:click={increment}>increment </button></div>
  <p>count is {count}</p>
  <div><button on:click={decrement}>decrement</button></div>
</main>

<style>
</style>
