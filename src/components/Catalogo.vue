<template>
  <div class="bg-secondary-100 flex-1 ml-48">
    <div class="mx-auto max-w-2xl px-4 sm:px-6 lg:max-w-7xl lg:px-8">
      <h2 class="text-2xl font-bold tracking-tight text-gray-900">Perfumes</h2>

      <div
        class="mt-6 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8"
      >
        <div
          v-for="product in products"
          :key="product.id"
          class="group relative"
        >
          <div
            class="aspect-h-1 aspect-w-1 w-full rounded-md bg-gray-200 lg:aspect-none group-hover:opacity-75 lg:h-80"
          >
            <img
              :src="product.imagem"
              :alt="product.imageAlt"
              class="h-full w-full object-cover object-center lg:h-full lg:w-full"
            />
          </div>
          <div class="mt-4 flex justify-between">
            <div>
              <h3 class="text-sm text-gray-700">
                <a :href="product.href">
                  <span aria-hidden="true" class="absolute inset-0" />
                  {{ product.nome }}
                </a>
              </h3>
              <p class="mt-1 text-sm text-gray-500">{{ product.marca }}</p>
            </div>
            <p class="text-sm font-medium text-gray-900">
              R$ {{ product.preco }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import axios from 'axios'

const products = ref([])
const error = ref(null)

const load = async () => {
  try {
    let data = await axios.get('/produtos')
    if (!data.status === 200) {
      throw new Error('Erro ao carregar os dados')
    }
    products.value = data.data
  } catch (err) {
    error.value = err.message
  }
}

load()
</script>
