<template>
  <footer>
    <div class="footer-logo">
      <img src="../assets/logo.png" alt="Logo" width="120px" />
    </div>

    <div class="footer-menu">
      <a href="#" class="fa fa-facebook" title="facebook"></a>
      <a href="#" class="fa fa-twitter" title="twitter"></a>
      <a href="#" class="fa fa-instagram" title="instagram"></a>
      <a href="#" class="fa fa-youtube" title="youtube"></a>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {}
  },
  methods: {},
}
</script>

<style>
body > footer {
  position: sticky;
  top: 100vh;
}

footer {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: crimson;
  width: 100%;
}

footer .footer-logo {
  justify-content: center;
  display: flex;
  align-content: center;
  padding: 5px;
}

footer .footer-logo img {
  height: 20px;
  width: auto;
  border-radius: 50%;
}

footer .footer-menu {
  position: absolute;
  right: 0;
  gap: 1rem;
  display: flex;
  margin: 0 1rem;
}

footer .footer-menu a {
  color: #000;
  display: flex;
  align-items: center;
  justify-content: center;
}

footer .footer-menu .fa {
  text-align: center;
  text-decoration: none;
  width: 1rem;
  height: 1rem;
  border-radius: 4px;
  color: white;
}

footer .footer-menu .fa:hover {
  opacity: 0.7;
}
</style>
