<template>
    <div :class="{'cliente': !isPremium, 'cliente-premium': isPremium }">
        <h4>Nome: {{ cliente.nome }}</h4>
        <hr>
        <p>E-mail: {{cliente.email }}</p>
        <hr>
        <p v-show="showIdade === true">Idade: {{ cliente.idade }}</p>
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
        color: rgb(160, 109, 109);
        background-color: black;
    }
</style>