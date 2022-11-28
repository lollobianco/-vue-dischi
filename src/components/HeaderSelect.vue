<template>
   <div>

      <select class="form-select form-select-sm" aria-label=".form-select-sm example">
         <option selected>Filter by musical genres</option>
         <option value="1">All</option>
         <option value="2">Rock</option>
         <option value="3">Pop</option>
         <option value="4">Jazz</option>
         <option value="5">Metal</option>
      </select>

   </div>
</template>

<script>
   export default {
      name: 'HeaderSelect'
   }
</script>

<style lang="scss" scoped>

</style>