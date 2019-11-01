<template>
  <div>
    <menubar/>
    <img src="../assets/Images/bitmap.png" class="banner"/>
  </div>
</template>

<script>
import MenuBar from './MenuBar'
export default {
  name: 'MainHeader',
  components: {
    menubar: MenuBar
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .banner {
    width: 100%;
  }
</style>
