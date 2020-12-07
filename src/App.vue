<template>
  <div id="app">


    <div class = "'container-fluid'">
      <div class="row row-cols-1 row-cols-md-2">
            <div class="col mb-4">
        <section-api></section-api>
      </div>
      </div>
    
    </div>
  
  

  
    <section id="team" class="equipo">
      <div class="card-group">


        <team-card  v-for="(item, index) of team" :key="index" :member ="team[index]" ></team-card>

      </div>
  | </section>

    <page-footer></page-footer>
 
</div>
</template>

<script>

import TeamCard from './components/TeamCard.vue'

import SectionApi from './components/SectionApi.vue'


import PageFooter from './components/PageFooter.vue'

export default {
  name: 'App',
  components: {
    TeamCard,
    PageFooter,
    SectionApi,

  },

  data(){
    return{
      title: 'Equipo de desarrollo',
      team: [
        {
         codigo: 1,
         nombre: "Edwin Camilo Reina Beltrán",
         descripcion: "Ingeniero mecánico con ínfulas de programador, runner en formación y con alta toleracia a la frustración (hincha de millonarios).",
         rol: "Desarrollador",
         image: "./assets/hulk.jpg",
        },
        {
         codigo: 2,
         nombre: "Felipe Agudelo Vélez",
         descripcion: "Ingeniero electrónico.... 31 desde que me descongelaron...practico treking aficionado.",
         rol: "Desarrollador",
         image: "./assets/capitan.jpg",
        },
        {
         codigo: 3,
         nombre: "Luz Dilma Barbosa Bautista",
         descripcion: "",
         rol: "Desarrollador",
         image: "./assets/marvel.jpg",
        },
        {
         codigo: 4,
         nombre: "Mateo Cañón Chisaba",
         descripcion: "Lingüista, bobo de profesion y medio editor de corazón, músico y odio programar.",
         rol: "Desarrollador",
         image: "./assets/thor.jpg",
        }
      ]
    }
  }
}
</script>

