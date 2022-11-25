<template>
   <div class="album">
      <img :src="albums.poster" alt="copertina album">
      <div class="title text-white fw-bold">{{albums.title.toUpperCase()}}</div>
      <div class="author subtitle-color">{{albums.author}}</div>
      <div class="subtitle-color">{{albums.year}}</div>
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
.album{
   // height: 200px;
   width: calc(90%/5);
   background-color: #2D3A46;
   padding: 15px;
   text-align: center;
   margin-top: 30px;

   div{
      background-color: #2D3A46;
   }

   img{
      width: 100%;
      margin-bottom: 20px;
   }
}

.subtitle-color{
   color: #6C6B6D;
}
</style>