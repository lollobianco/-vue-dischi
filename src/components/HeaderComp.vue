<template>
  <div id="header-component">

    <div id="logo-container">
      <img src="../assets/logo-small.svg" alt="">
    </div>
    
    
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

</style>
