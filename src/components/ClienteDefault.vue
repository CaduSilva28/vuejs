<template>
    <div id="clienteFull">
        <h4>Nome: {{ cliente.nome }}</h4>
        <hr>
        <p>E-mail: {{cliente.email }}</p>
        <hr>
        <!-- Aqui não vai mostrar a idade escondida
        <p v-if="showIdade === true">Idade: {{ cliente.idade }}</p>
        <p v-else>O usuário escondeu a idade</p>
        -->

        <!-- Aqui vai mostrar a idade escondida caso o usuário abra o html -->
        <p v-show="showIdade === true">Idade: {{ cliente.idade }}</p>
    </div>
</template>

<script>
export default {
    data(){
        return {
            numero: "48998384736",
            descricao: "lorem ipsum lorem ipsum"
        }
    },
    props: {
        cliente: Object,
        showIdade: Boolean
    }
}
</script>

<style scoped>
    #clienteFull{
        color: blue;
        background-color: antiquewhite;
        padding: 10px;
        margin-top: 10px;
    }

    .cliente-nome{
        color: rgb(160, 109, 109);
    }
</style>