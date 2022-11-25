<template>
  <div id="app">

    <HeaderComp/>
    <AlbumComp/>

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
        albums: ''
      }
    },
    mounted() {
  
      this.getAlbums();

    },
    methods: {

      getAlbums() {

        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
          .then((response) => {
            this.albums = response.data
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
