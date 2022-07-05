<template>
  <div id="app">
    <NavBar />
    <div class="container">
      <div class="row">
        <div class="col-md-2" v-for="image in images" :key="image">
          <ImagePanel :imgSource="image.src" :imgName="image.imgName" :artistName="image.artistName"/>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import NavBar from './components/NavBar.vue'
import ImagePanel from './components/ImagePanel.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    ImagePanel
},
data() {
    return {
      images: [
        {src: "logo.png", imgName: "Logo", artistName: "Ben X"},
        {src: "me.jpg", imgName: "Me", artistName: "Ben W"},
        ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
