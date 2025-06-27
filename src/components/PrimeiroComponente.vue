<template>
    <div class="meuComponente">
        <h2>{{ titulo }}</h2>
        <p>{{ descricao }}</p>
        <button @click="alterarTitulo">Alterar Título</button>
    </div>
</template>

<script>
    export default{
        name: 'Primeiro Componente',
        data(){
            return{
                titulo: 'Olá, Vue!',
                descricao: 'Este é o meu primeiro componente Vue.'
            }
        },
        methods:{
            alterarTitulo(){
                this.titulo = "Título Alterado"
            }
        }
    }
</script>

<style scoped>
    .meuComponente{
        border: 2px solid orangered;
        border-radius: 8px;
        padding: 20px;
        margin: 20px;
    }

    h2{
        color: orangered;
    }

    button{
        border-radius: 5px;
        padding: 5px;
    }
</style>