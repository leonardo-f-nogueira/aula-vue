<template>
    <div class="cartao-usuario">
        <h3>{{ nome }}</h3>
        <p><b>Idade: </b>{{ idade }}</p>
        <p><b>E-mail: </b>{{ email }}</p>
        <p><b>Status: </b>
            <span :class="statusClass">{{ statusTexto }}</span>
        </p>

    </div>
</template>

<script>
    export default{
        name: 'CartaoUsuario',
        props:{
            nome:{
                type: String,
                required: true
            },
            idade:{
                type: Number,
                required: true
            },
            email:{
                type: String,
                required: true
            },
            ativo:{
                type: Boolean,
                default: true
            }
        },
        computed:{
            statusClass(){
                return this.ativo ? 'status-ativo' : 'status-inativo'
            },
            statusTexto(){
                return this.ativo ? 'Ativo' : 'Inativo'
            }
        }
    }

</script>

<style scoped>

.cartaoUsuario{
    border: 2px solid blue;
    border-radius: 8px;
    padding: 15px;
    margin: 10px;
    background-color: #fff8dc;
}

.status-ativo{
    color: rgb(10, 218, 10);
    font-weight: bold;
}

.status-inativo{
    color: red;
    font-weight: bold;
}
</style>