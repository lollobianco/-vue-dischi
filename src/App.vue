<template>
  <div id="app">

    <HeaderComp/>

  </div>
</template>

<script>
import axios from 'axios'
import HeaderComp from './components/HeaderComp.vue'

export default {
  name: 'App',
  components: {
    HeaderComp
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
