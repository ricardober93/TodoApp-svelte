<script>
  import ListTodos from "./components/ListTodos.svelte";
  import Nabvar from "./components/Nabvar.svelte";
  import Form from "./components/Form.svelte";
  let todos = [];
  function updateTodos(todo) {
    todos = [...todos, todo];
  }

  function deleteTodo(name) {
    todos = todos.filter((t) => t.name !== name);
    console.log(todos);
  }
</script>

<style>
  .grid {
    display: flex;
    grid-template-columns: 1fr 2fr;
    gap: 20px;
  }
</style>

<Nabvar name="Ricardo" />
<main class="grid">
  <Form {updateTodos} />
  <ListTodos {todos} {deleteTodo} />
</main>
