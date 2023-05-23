<template>
  <div class="catalogo">
    <section id="perfumes">
      <h2>Perfumes</h2>
      <ul class="lista-perfumes">
        <!--<li v-for="produto in produtos">
          <img :src="produto.imagem" alt="Perfume" />
          <p>R$ {{ produto.preco }},00</p>
        </li>-->
      </ul>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Catalogo',
  components: {},
}
</script>

<style scoped>
.catalogo {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  margin-right: 1rem;
  gap: 1rem;
}

section {
  width: 100%;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
}

section ul {
  flex-wrap: wrap;
  display: flex;
  justify-content: flex-start;
  margin: 0;
  padding: 0 10px;
  overflow: auto;
  gap: 1rem;
  padding-bottom: 1rem;
}

section ul li {
  list-style-type: none;
  transition: 0.2s;
}

section ul li:hover {
  background-color: #fff;
  box-shadow: 0px 6px 16px 0px rgb(0 0 0 / 40%);
}

section li a,
section li a:hover {
  text-decoration: none;
  color: #000;
}

section h2 {
  margin-left: 1rem;
  font-size: 1.7rem;
  color: var(--h);
}

section {
  background-color: var(--rosa);
}

section li {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 0px 0px 5px 0px !important;
  margin-block: 0;
  margin-inline: 0;
  background-color: #fff;
  padding: 10px;
  border-radius: 8px;
  gap: 0.5rem;
}

section li img {
  width: 7rem;
  height: auto;
  border-radius: 8px;
}

section li p {
  font-size: 14px;
  font-weight: 500;
  margin: 0;
  text-align: center;
}

.botao-mais-produtos {
  border-radius: 8px;
  border: none;
  padding: 5px 10px;
  font-size: small;
  width: fit-content;
  color: #fff;
  background-image: url('../../public/img/background-color-rose.png');
  align-self: flex-end;
  margin: 0px 10px 10px 0px;
}
</style>
