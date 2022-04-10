<script setup>
import Header from './components/Header.vue';
import Menu from './components/Menu.vue';
import Movie from './components/Movie.vue';
</script>

<template>
<div id="form">
<Header title="Chose a TV show:" />
<Menu @clicked="onCallApi" />
</div>
<div id="container">
<Movie  :movies ="arrayTest"/>
</div>
</template>

<script>
export default {
  name:'App',
  components: {
    Header,
    Menu,
    Movie
  },
  data(){
    return{
    arrayTest :[]
    }
  },
  methods:{
    onCallApi(array){
      this.arrayTest=array

    }
  }
  }
</script>

<style>
*{
   font-family: Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu,
    Cantarell, 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
    margin: 0;
    padding: 0;
}
.btn{
  font-size: 15px;
  padding: 9px;
  border:none;
  background-color:red;
  color:white;
  cursor:pointer;
}
.inp{
  font-size: 15px;
  padding:9px;
  border:none;
  background-color:white;
}
body{
  display:flex; 
  place-items: center;
  justify-content: center;
  flex-direction: column;
  width:auto;
  height: auto;
  font-size: 15px;
  line-height: 1.6;
  background-color: black;
}
  .movie{
    /* padding: 10px; */
    margin: 15px;
    text-align: center;
    background-color: rgba(97, 95, 95, 0.13);
    border-radius: 1.5rem;
    color: white;

  }
  #delete{
    background-color: white;
    border:none;
    margin-left:20rem;
    display:block;
    font-size: 15px;
  }
  #form{
    text-align: center;
  }
  #container{
    display:flex;
    flex-wrap: wrap;
    justify-items: center;
    align-items: center;
  }
   #app {
  max-width: 80%;
  padding: 2rem;
   }

</style>
