<template>
  <div id="app">

    <HeaderComp/>

    <div class="card-container">
      <div class="d-flex flex-wrap justify-content-center justify-content-between">
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
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: #1E2D3B;
}

#app {
  
}

.card-container{
  width: 70%;
  margin: 0 auto;
  padding: 0;
}

.row{
  width: 100%;
  margin: 0 auto;
}
</style>
