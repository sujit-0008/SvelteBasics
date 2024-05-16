<script>
  import Hero from "../lib/hero.svelte";
  let todos = [];
  let todotask;
  const addTodo = () => {
    if (todotask.trim() != "") {
      todos = [...todos, { id: Date.now(), text: todotask }];
      todotask = "";
    }
  };
  const removetodo = (id) => {
    todos = todos.filter((item) => item.id != id);
  };
</script>

<main>
  <Hero msg="This is TODO " />
  <div>
    <input type="text" bind:value={todotask} placeholder="Enter task name " />
    <button on:click={addTodo}>Add Todo</button>
  </div>

  {#if todos.length > 0}
    {#each todos as todo}
      <ul>
        <li>
          <span>{todo.text} </span>
          <button on:click={() => removetodo(todo.id)}>RemoveTodo</button>
        </li>
      </ul>
    {/each}
  {:else}
    <p>No data Found</p>{/if}
</main>

<style>
  ul {
    list-style: none;
    padding: 0;
  }

  li {
    margin: 10px 0;
  }
</style>
