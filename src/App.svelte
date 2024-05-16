<script>
  import { Router, Route, Link } from "svelte-routing";
  import Counter from "./pages/Counter.svelte";
  import List from "./pages/List.svelte";
  import ToDo from "./pages/to-do.svelte";
  import Nav from "../src/lib/nav.svelte";
  import Parent from "./pages/parent.svelte";
</script>

<main>
  <Router>
    <Nav />
    <Route path="/" component={Counter} />
    <Route path="/todo" component={ToDo} />
    <Route path="/list" component={List} />
    <Route path="/parent" component={Parent} />
  </Router>
</main>
