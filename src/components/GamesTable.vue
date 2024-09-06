<template>
  <div>
    <table class="table table-dark">
        <thead>
          <tr>
            <th scope="col">#</th>
            <th scope="col">Expansión</th>
            <th scope="col">Eliminar juego de tu lista</th>
          </tr>
        </thead>
        <tbody>
         <Game
         v-for="game in games"
         :id="game.id"
         :key="game.id"
         :name="game.name"
         @eliminar="deleteGame"></Game>
        </tbody>
    </table>
    <section v-if="games.length == 0" class="container mx-auto p-2 noGame">
      <div class="row d-flex justify-content-center">
        <h2 class="col-7">No tienes juegos en tu lista</h2>
        <button class="section__button col-4 p-1" @click="refresh">Refrescar</button>
      </div>
    </section>
  </div>
</template>

<script>
import Game from "./Game.vue"
export default {
    name: 'gamesTable-comp',
    // props: {},
    data: function(){
        return {
          games:[
                {id:1, name:"Get to Work"},
                {id:2, name:"Cats & Dogs"},
                {id:3, name:"Discover University"},
                {id:4, name:"Seasons"},
          ]
        }
    },
    // computed: {},
    methods: {
      deleteGame(id){
        let i = this.games.findIndex(game=> game.id == id)
        this.games.splice(i,1)
      },
      refresh(){
        window.location.reload()
      }
    },
    // watch: {},
    components: {
      Game
    },
    // mixins: [],
    // filters: {},
    // -- Lifecycle Methods
    // -- End Lifecycle Methods
}
</script>

<style scoped>
th{
  border: 2px solid white;
}
.noGame{
  background-color: greenyellow;
}
.section__button{
  border: none;
  border-radius: 5px;
  background-color: darkblue;
  color: white;
  font-weight: 500;
}
    
</style>