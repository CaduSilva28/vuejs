<template>
  <h1>Guia Clientes</h1>
  <ClienteDefault/>
  <hr>
    <h4>Lista de produtos</h4>
  <hr>
  <ProdutosDefaultVue/>
</template>

<script>
import ClienteDefault from './components/ClienteDefault.vue';
import ProdutosDefaultVue from './components/ProdutosDefault.vue';

export default {
  name: 'App',
  components: {
    ClienteDefault,
    ProdutosDefaultVue
  }
}
</script>

<style>

</style>
