<script>
  export let todos;
  export let deleteTodo;

  function hanlderClick(name) {
    deleteTodo(name);
  }
</script>

<style>
  .grid {
    width: 100%;
    display: grid;
    padding: 0.5em;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 20px;
    align-items: center;
    justify-content: center;
  }

  .card {
    width: 180px;
    display: flex;
    grid-template-columns: subgrid;
    border: 1px solid rgba(0, 0, 0, 0.2);
    padding: 0.6m;
    font-size: 0.7em;
    align-items: center;
    height: 28px;
  }
  h3 {
    font-size: 1.3em;
    font-weight: 800;
    margin-right: 0.3em;
  }

  p {
    width: 100%;
    font-size: 1.2em;
    font-weight: 700;
    color: grey;
  }
  button {
    background-color: red;
    color: white;
    height: inherit;
    font-size: 12px;
    padding: 0.1em 0.3em;
    display: flex;
    place-items: center;
    border: none;
  }
</style>

<section class="grid">

  {#each todos as { name, description }}
    <div class="card">
      <h3>{name}</h3>
      <p>{description}</p>
      <button on:click={() => hanlderClick(name)}>Eliminar</button>
    </div>
  {:else}
    <p>Aun no Tienes tareas</p>
  {/each}
</section>
