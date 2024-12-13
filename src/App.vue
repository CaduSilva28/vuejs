<template>
  <h1>Guia Clientes</h1>
  <div v-for="(cliente,index) in clientes" :key="cliente.id">
    <h5>{{index + 1}}</h5>
    <ClienteDefault :cliente="cliente"/>
    <h4>Edição</h4>
    <input type="text" v-model="cliente.nome">
    <input type="text" v-model="cliente.email">
  </div>
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
      },
      clientes: [
        {
          id: 1,
          nome: "Carlos Eduardo",
          email: "carloseduardo@gmail.com",
          idade: 30
        },
        {
          id: 2,
          nome: "João Pedro",
          email: "joaopedro@gmail.com",
          idade: 21
        },
        {
          id: 3,
          nome: "Luiza Souza",
          email: "luizasouza@gmail.com",
          idade: 33
        },
      ]
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
