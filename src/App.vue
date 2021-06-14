<template>
<div id="app">
  <!-- Header -->
  <div class="header">
    <div class="header-left">
    <div class="icon">
     <img src="./assets/tmdb.svg" alt="tmdb"
      height="20px"
      width="154"
     >
  </div>
      <div class="dropdow">Movies</div>
      <div class="dropdow">TV Shows</div>
      <div class="dropdow">People</div>
      <div class="dropdow">More</div>
   </div>
   <div class="header-right">
     <div class="item">EN</div>
     <div class="item">Login</div>
     <div class="item">Join TMDb</div>
   </div>
 </div>
 <!-- List -->
 <h2>Popular Movies</h2>
<div class="container">
  <list
  v-for="(card,index) in cards"
  :key="index"
  :card="card" 
  :index="index"
  />
</div>
<div class="loadmore">Load More</div>
</div>
</template>
 <script>
 import List from './components/List.vue'
  export default {
  name: 'App',
  data(){
    return {
      cards:[
        {
        title: 'Cruella',
        date:'May 26, 2021',
        src: require('./assets/movie.jpg')
        },

        {
        title: 'Those Who Wish Me Dead',
        date:'May 05, 2021',
        src: require('./assets/movie1.jpeg')
        },

        {
        title: 'Mortal Kombat',
        date:'Arp 07, 2021',
        src: require('./assets/movie2.jpeg')
        },

        {
        title: "Tom Clancy's Without Remorse",
        date:'Arp 29, 2021',
        src: require('./assets/movie3.jpeg')
        },
        
        {
        title: 'Godzilla vs Kong',
        date: 'Mar 24, 2021',
        src: require('./assets/movie4.jpeg')
        }
      ]
    }
  },
  components: {
    List
  }
}
</script>

<style>
/* Header */
*{
  box-sizing: border-box;
  font-size: 15px;
  font-family: "Source Sans Pro", Arial, sans-serif;
  font-weight: bold;
  padding: 0;
  margin: 0;
}
.header{
  display: flex;
  justify-content: space-between;
  color: white;
  background:#032541;
  height: 64px;
  width: 100%;
}
.header-left, .header-right{
  display: flex;
  align-items: center;
}
.dropdow{
  display: flex;
  align-items: center;
  cursor: pointer;
  padding: 1rem;
}
.item{
  display: flex;
  align-items: center;
  cursor: pointer;
  padding: 1rem;
}
.icon{
  padding: 2rem;
  cursor: pointer;
}
.loadmore{
  padding: 15px;
  display: flex;
  justify-content: center;
  background-color: #05b3e4;
  color: white;
  font-size: 1.5rem;
  margin: 2rem;
  margin-top: 1.5rem;
  border-radius: 5px;
}
/* List */
</style>
