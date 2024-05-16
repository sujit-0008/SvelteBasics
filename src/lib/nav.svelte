<script>
  import { Link } from "svelte-routing";
</script>

<nav>
  <ul>
    <li><Link to="/">Counter</Link></li>
    <li><Link to="/list">List Rendering</Link></li>
    <li><Link to="/todo">TO-Do List</Link></li>
    <li> <Link to='/parent'>Prop-eventDispatch</Link>

    </li>
  </ul>
</nav>

<style>
  nav {
    background: #333;
    color: white;
    padding: 1em;
    padding: auto;
  }
  ul {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;

  }
</style>
