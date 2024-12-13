<template>
  <h3>Cadastro: </h3>
  <small id="nomeErro" v-show="deuErro">Digite alguma coisa, querido</small><br>
  <input type="text" placeholder="nome" v-model="nomeField"> <br>
  <input type="email" placeholder="email" v-model="emailField"> <br>
  <input type="number" placeholder="idade" v-model="idadeField"> <br>
  <button @click="cadastrarUsuario">Cadastrar</button>
  <div v-for="(cliente,index) in clientes" :key="cliente.id">
    <h5>{{index + 1}}</h5>
    <ClienteDefault :cliente="cliente"/>
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
      deuErro: false,
      nomeField: "",
      emailField: "",
      idadeField: 0,
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
        }
      ]
    }
  },
  components: {
    ClienteDefault,
    ProdutosDefaultVue
  },
  methods: {
    cadastrarUsuario: function(){
      if(!this.nomeField || !this.emailField || !this.idadeField){
        this.deuErro = true
      }else{
         this.clientes.push({ 
          nome: this.nomeField, 
          email: this.emailField, 
          idade: this.idadeField,
          id: Date.now()
        })
        this.deuErro = false;
      }
      
      //Limpando os campos cadastrados
      this.nomeField = "";
      this.emailField = "";
      this.idadeField = "";
    }
  }
}
</script>

<style>
  #nomeErro{
    color: red;
  }
</style>
