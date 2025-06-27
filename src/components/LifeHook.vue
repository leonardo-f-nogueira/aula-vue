<template>
    <div class="life-hook">
        <h3>{{ mensagem }}</h3>
        <p>Dados: {{ dados }}</p>
        <button @click="atualizarDados">Atualizar Dados</button>
    </div>
</template>

<script>
    export default {
        name: 'LifeHook',
        data(){
            return{
                mensagem: 'Demonstração dos Life Hooks',
                dados: 'Dados iniciados'
            }
        },
        beforeCreate(){
            console.log("beforeCreate: Componente está sendo criado.")
            
        },
        created(){
            setTimeout(()=>{
                this.dados = 'Dados inicializados'
            }, 5000)
        },
        mounted(){
            console.log("mounted: Quando o componente está sendo montado na tela.")
            //Ideal para manipular DOM
            
        },
        updated(){
            console.log("updated: Componente está sendo atualizado.")
        },
        methods:{
            atualizarDados(){
                this.dados = 'Dados atualizados - ' + new Date().toLocaleTimeString
            }
        
        }
    }
</script>

<style scoped>

</style>