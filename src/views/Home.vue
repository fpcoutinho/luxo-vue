<template>
  <main>
    <Sidebar />
    <Catalogo />
  </main>
</template>

<script>
// @ is an alias to /src
import Sidebar from '@/components/Sidebar.vue'
import Catalogo from '@/components/Catalogo.vue'

export default {
  name: 'Home',
  components: {
    Sidebar,
    Catalogo,
  },
}
</script>

<style scoped>
::-webkit-scrollbar {
  width: 10px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
  background: crimson;
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: crimson;
}

main {
  display: flex;
  overflow: scroll;
  gap: 1rem;
}

main::-webkit-scrollbar {
  display: none;
}

/* Esconder scrollbar em: IE, Edge e Firefox */
main {
  -ms-overflow-style: none; /* IE e Edge */
  scrollbar-width: none; /* Firefox */
}
</style>
