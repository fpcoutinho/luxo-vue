<template>
  <nav class="sidebar">
    <h2>Categorias</h2>
    <ul>
      <li><a href="#">Perfumes</a></li>
      <li><a href="#">Maquiagens</a></li>
      <li><a href="#">Cabelos</a></li>
      <li><a href="#">Pele</a></li>
      <li><a href="#">Cuidados</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Sidebar',
  components: {},
}
</script>

<style>
.sidebar {
  width: 200px;
  height: 100%;
  background-color: crimson;
  border-radius: 0 8px 8px 0;
  padding: 20px 10px;
  box-sizing: border-box;
  color: #fff;
}

.sidebar h2 {
  margin-top: 0;
}

.sidebar ul {
  list-style: none;
  padding: 0;
  margin: 20px 0;
}

.sidebar ul li {
  background-color: #ffc6c6;
  padding: 5px 10px;
  margin-bottom: 10px;
  color: #fff;
  border-radius: 8px;
}

.sidebar ul li a {
  display: block;
  width: 100%;
  text-decoration: none;
  color: var(--h);
  transition: 0.6s ease-in;
}

.sidebar ul li:hover {
  transition: 0.3s ease-in;
  box-shadow: 0px 6px 16px 0px rgb(0 0 0 / 40%);
  opacity: 0.8;
}
</style>
