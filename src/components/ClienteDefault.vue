<template>
    <div id="cliente">
        <h1>Meus inputs</h1>
        <input type="text" v-model="nome">
        <hr>
        <input type="text" v-model="descricao">
        <br>
        <br>
        <br>
        
        <h2 class="cliente-nome">Nome do cliente: {{ nome }}</h2>
        <hr>
        <h2 class="cliente-nome">Descrição: {{ descricao }}</h2>
        <h2 class="cliente-nome">Descrição: {{ descricao }}</h2>
        <h2 class="cliente-nome">Descrição: {{ descricao }}</h2>
        <h2 class="cliente-nome">Descrição: {{ descricao }}</h2>
        <hr>
    </div>
</template>

<script>
export default {
    data(){
        return {
            nome: "Carlos Eduardo da Silva",
            numero: "48998597171",
            email: "",
            idade: 0,
            descricao: "lorem ipsum lorem ipsum"
        }
    }
}
</script>

<style scoped>
    #cliente{
        color: blue;
        background-color: antiquewhite;
    }

    .cliente-nome{
        color: rgb(160, 109, 109);
    }
</style>