<template>
  <div id="app">

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
import PageFooter from './components/PageFooter.vue'

export default {
  name: 'App',
  components: {
    TeamCard,
    PageFooter
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
         imagen: "../assets/hulk.jpg",
        },
        {
         codigo: 2,
         nombre: "Felipe Agudelo Vélez",
         descripcion: "Ingeniero electrónico.... 31 desde que me descongelaron...practico treking aficionado.",
         rol: "Desarrollador",
         imagen: "../assets/capitan.jpg",
        },
        {
         codigo: 3,
         nombre: "Luz Dilma Barbosa Bautista",
         descripcion: "",
         rol: "Desarrollador",
         imagen: "../assets/marvel.jpg",
        },
        {
         codigo: 4,
         nombre: "Mateo Cañón Chisaba",
         descripcion: "Lingüista, bobo de profesion y medio editor de corazón, músico y odio programar.",
         rol: "Desarrollador",
         imagen: "../assets/thor.jpg",
        },
        {
         codigo: 5,
         nombre: "Franyer",
         descripcion: "Dejó el grupo de forma inesperada. Te recordaremos siempre...",
         rol: "Desertor",
         imagen: "../assets/tony.jpg",
        }
      ]
    }
  }
}
</script>

