<template>
   <div id="album" class="col-2">
      <img :src="albums.poster" alt="copertina album">
   </div>
</template>

<script>
   export default {
      name: 'AlbumComp',
      props: {
         albums: Object
      }
   }
</script>

<style lang="scss" scoped>

</style>