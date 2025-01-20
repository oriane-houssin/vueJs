<script lang="ts">
import { ref } from 'vue'
export default {
  name: 'ProductList',
  setup() {
    interface Product {
      id: number
      label: string
      description: string
      qte: number
    }
    const echalotte = ref<Product>({id: 0, label: 'echalotte', description: 'echalotte', qte: 6})
    const carotte = ref<Product>({ id: 1, label: 'carotte', description: 'carotte', qte: 5 })
    const courgette = ref<Product>({ id: 2, label: 'courgette', description: 'courgette', qte: 3 })
    const pdt = ref<Product>({ id: 3, label: 'pomme de terre', description: 'pdt', qte: 10 })
    const oignon = ref<Product>({ id: 4, label: 'oignon', description: 'oignon', qte: 0 })
    const liste = [echalotte, carotte, courgette, pdt, oignon]
    return { liste, carotte }
  },
}
</script>
<template>
  <div>{{ carotte }}</div>
</template>
<style></style>
