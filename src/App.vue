<template>
  <div id="app">
    <nav class="nav container-fluid justify-content-center p-2">
      <div class="row ">
        <h1 class="nav__title">Tienda Bit-Game</h1>
      </div>
    </nav>
    <header class="header container my-5">
        <div class="header__content rounded px-4 py-3">
          <h2 class="header__title pb-2">¡Bienvenido a Sims 4!</h2>
          <hr>
          <p class="header__text align-self-end mb-0">A continuación encontrarás la lista de expansiones que prefieres</p>
        </div>
    </header>
    <section class="container-fluid ">
      <div class="row col-10 mx-auto">
        <GamesTable></GamesTable>
      </div>
    </section>    
  </div>
</template>

<script>
import GamesTable from "./components/GamesTable.vue"
export default {
  name: 'App',
  
  components: {
    GamesTable
  },
}
</script>

<style>
.nav{
  background-color: rgb(39, 36, 36);
  color: #fff;
}
.nav__title{
  font-weight: 400;
  font-size: 1.5rem;
}
.header__content{
  background-color: rgb(197, 240, 241);
  color: rgb(0, 70, 136);
}



</style>
