<script>
  export let updateTodos;
  let name;
  let description;

  function addTodo(params) {
    let todo = {
      name: name,
      description: description,
    };
    console.log(todo);
    updateTodos(todo);

    name = "";
    description = "";
  }
</script>

<style>
  form {
    display: grid;
    gap: 20px;
    padding: 1em;
    max-height: 150px;
  }
</style>

<form>
  <input bind:value={name} type="text" placeholder="agrega una tarea" />
  <input
    bind:value={description}
    type="text"
    placeholder="agrega una descripion" />
  <button on:click={addTodo} type="button">Agregar tarea</button>
</form>
