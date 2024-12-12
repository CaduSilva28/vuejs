<template>
  <h1>Guia Clientes</h1>
  <input type="text" v-model="clienteCadu.idade">
  <ClienteDefault :cliente="clienteCadu" :showIdade="true"/>
  <ClienteDefault :cliente="clienteCadu" :showIdade="false"/>
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
  data(){
    return {
      nomeDoCadu: "Carlos Sauro",
      clienteCadu: {
        nome: "Carlos Eduardo",
        email: "marioeduardo@gmail.com",
        idade: 35
      }
    }
  },
  components: {
    ClienteDefault,
    ProdutosDefaultVue
  }
}
</script>

<style>

</style>
