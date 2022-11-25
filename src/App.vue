<template>
  <div id="app">

    <HeaderComp/>

    <div class="container">
      <div class="row">
        <AlbumComp v-for="(element, ind) in albumsArray" :key="ind" :albums="element"/> 
      </div>
    </div>

    
    

  </div>
</template>

<script>
import axios from 'axios'
import HeaderComp from './components/HeaderComp.vue'
import AlbumComp from './components/AlbumComp.vue'


export default {
  name: 'App',
  components: {
    HeaderComp,
    AlbumComp
  },
  data() {
      return {
        albumsArray: ''
      }
    },
    mounted() {
  
      this.getAlbums();

    },
    methods: {

      getAlbums() {

        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
          .then((response) => {
            this.albumsArray = response.data.response
            console.log(this.albumsArray)
          })

      }
    }
}
</script>

<style lang="scss">
#app {
  height: 100vh;
  background-color: #1E2D3B;
}
</style>
