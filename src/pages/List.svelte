<script>
  ; import Hero from "../lib/hero.svelte";

  let users = [
    { id: 1, name: "sujit", email: "sujittingare@gmail.com" },
    { id: 2, name: "digvijay", email: "sdigvijay@gmail.com" },
    { id: 3, name: "anil", email: "anil@gmail.com" },
  ];
  const getuser = () => {
    return users;
  };
</script>

<main>
  <Hero msg="This is List Render"/>
  {#if getuser().length > 0}
    {#each getuser() as { id, name, email }, index}
      <div>
        <li><span>{id}</span> <span>{name}</span></li>
        <li>{email}</li>
      </div>
    {/each}
  {:else}
    <p>User not found</p>
  {/if}
</main>

<style>
  div {
    padding: 10px;
    margin: 5px;
    border: 1px solid white;
  }
</style>
