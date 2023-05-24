<template>
  <main class="flex gap-4 no-scrollbar">
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
