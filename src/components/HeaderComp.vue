<template>
  <div id="header-component">

    <div id="logo-container">
      <img src="../assets/logo-small.svg" alt="">
    </div>

    <HeaderSelect/>
    
  </div>
</template>

<script>
import HeaderSelect from './HeaderSelect.vue'

export default {
  name: 'HeaderComp',
  components:{
    HeaderSelect
  },
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

</style>
