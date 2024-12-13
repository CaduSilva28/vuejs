<template>
    <div :class="{'cliente': !isPremium, 'cliente-premium': isPremium }">
        <h4>Nome: {{ cliente.nome }}</h4>
        <hr>
        <p>E-mail: {{cliente.email }}</p>
        <hr>
        <p>Idade: {{cliente.idade }}</p>
        <hr>
        <p v-show="showIdade === true">Idade: {{ cliente.idade }}</p>
        <button @click="mudarCor($event)">Mudar cor</button>
    </div>
</template>

<script>
export default {
    data(){
        return {
            numero: "48998384736",
            descricao: "lorem ipsum lorem ipsum",
            isPremium: true
        }
    },
    props: {
        cliente: Object,
        showIdade: Boolean
    },
    methods: {
        mudarCor: function($event){
            //O this indica: Neste componente, pegue a veariável tal
            console.log($event);
            this.isPremium = !this.isPremium
        }
    }
}
</script>

<style scoped>
    .cliente{
        color: blue;
        background-color: antiquewhite;
        padding: 10px;
        margin-top: 10px;
    }

    .cliente-premium{
        color: rgb(255, 255, 255);
        background-color: rgb(63, 104, 187);
    }
</style>