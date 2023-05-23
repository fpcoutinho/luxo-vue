<template>
  <Header />
  <router-view />
  <Footer />
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
  },
}
</script>

<style>
:root {
  --bg: #fff;
  --header-bg: #ffc6c6;
  --primary: #0f172a;
  --secondary: #334155;
  --h: #7f1d1d;
  --h-hover: #991b1b;
  --label: #64748b;
  --cards: #f4f6f8;
  --vermelho: #ee223b;
  --rosa: #ffc6c6;
}

html {
  background-color: var(--bg);
  color: var(--primary);
  height: 100%;
}

body {
  font-size: 16px;
  line-height: 1.5;
  margin: 0;
  height: 100%;
}

main {
  padding-top: 100px;
  padding-bottom: 1rem;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
}

@media only screen and (max-width: 600px) {
  body {
    grid-template-columns: 1fr;
  }
  header {
    grid-column: 1/1;
  }
  main {
    grid-column: 1/1;
    gap: 1rem;
  }
  footer {
    grid-column: 1/1;
    align-items: center;
    justify-content: center;
  }
  article {
    gap: 0px;
  }
  section {
    border-radius: 0%;
    align-items: center;
  }
  ul {
    padding-left: 0px;
  }
  section h2 {
    font-size: 1.5rem;
    text-align: center;
  }
  .botao-mais-produtos {
    border-radius: 0%;
  }
  .pagina-top {
    flex-direction: column-reverse;
  }
  .menu-vertical {
    width: 100%;
  }
  .busca-div {
    width: 100%;
  }
  .busca-div span {
    display: none;
  }
  .busca-div input {
    width: 88%;
    border-radius: 0px;
    height: 2rem;
  }
  .footer-menu {
    display: none;
  }
  .nav-header {
    display: none;
  }
}
</style>
