<template>
    <div class="movie" :id="index" :key="index" v-for="(movie, index) in movies" >
        <button id="delete" @click=deleteE(index) style="font-weight:bold; cursor:pointer;background-color:transparent; color:white;"> &#10006;</button>
        <img :src= "movie.data.image.medium" style="border-radius:5px" />
        <p>Name: {{movie.data.name}}</p>
        <p>Genres: {{movie.data.genres}}</p>
        <p>Avarage rating: {{movie.data.rating.average}}</p>
    </div>
 
</template>

<script>
import menu from './Menu.vue'

export default{
    name: 'Movies',
    props:{
        movies: Array,
    },
  conponents:{
      menu
  },
  data(){
      return{
        
  }
  },
  methods:{
      deleteE(index){
          this.movies.splice(index,1)
   
      },
}
  }

</script>
