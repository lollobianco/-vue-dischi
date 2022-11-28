<template>
  <div id="header-component">

    <div id="logo-container">
      <img src="../assets/logo-small.svg" alt="">
    </div>

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
  name: 'HeaderComp',
  props: {
    
  }
}
</script>


<style scoped lang="scss">

#header-component{
  height: 60px;
  background-color: #2D3A46;
  display: flex;
  align-items: center;
}

#logo-container{
  height: 60px;
  width: 60px;
  background-color: #2D3A46;
  display: flex;
  align-items: center;
  margin-left: 15px;

  img{
    background-color: #2D3A46;
    width: 80%;
  }

}

.form-select{
  width: 20%;
  margin-left: 20px;
}

</style>
