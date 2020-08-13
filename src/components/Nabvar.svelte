<script>
  export let name;
</script>

<style>
  nav {
    height: 60px;
    padding: 0 1.5em;
    background-color: #1b262c;
    color: #ffffff;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  li {
    text-decoration: none;
    list-style: none;
    font-size: 1.5em;
    font-weight: 800;
  }
</style>

<nav class="Nav">
  <li>LOGO</li>
  {name}
</nav>
