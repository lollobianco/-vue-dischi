<template>
   <div>

      <select class="form-select form-select-sm" aria-label=".form-select-sm example" v-model="filterGenre" @click="$emit ('select', filterGenre)">
         <option value="All">All</option>
         <option value="rock">Rock</option>
         <option value="pop">Pop</option>
         <option value="jazz">Jazz</option>
         <option value="metal">Metal</option>
      </select>

   </div>
</template>

<script>
   export default {
      name: 'HeaderSelect',
      props: {
         albums: Object
      },
      data(){

         return{
            filterGenre: ""
         };

      }
   
   };
</script>

<style lang="scss" scoped>

</style>