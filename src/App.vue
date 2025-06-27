<template>
  <div class="app">
    <h1>Demonstração de Props</h1>
    <CartaoUsuarioVue
      :nome="usuario.nome"
      :idade="usuario.idade"
      :email="usuario.email"
      :ativo="usuaio.ativo"/>
    <CartaoUsuarioVue
      :nome="Leonardo"
      :idade="27"
      :email='leonardo@email.com'/>
  </div>
</template>

<script>
  // import PrimeiroComponenteVue from './components/PrimeiroComponente.vue'
  // import LifeHookVue from './components/LifeHook.vue'
  import CartaoUsuarioVue from './components/CartaoUsuario.vue'
  export default{
    name: 'App',
    components:{
      // PrimeiroComponenteVue,
      // LifeHookVue,
      CartaoUsuarioVue
    },
    data(){
      return{
        usuario:{
          nome: 'Emilly Raiane',
          idade: 21,
          email: 'crazyemilly@outlook.com',
          ativo:false
        }
        }
      }
    }
</script>

<style scoped>
  .app{
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    text-align: center;
    margin-top: 60px;
  }
</style>
