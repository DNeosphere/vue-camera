<template>
  <div class="app">
    <main class="main">
      <h1>Hello World!</h1>
      <p>Upload a Photo!</p>

      <img
        @click="showCamera = true"
        class="camera-icon"
        src="https://img.icons8.com/dusk/344/26e07f/camera.png"
        alt="Camera icon">
    </main>
    <camera v-if="showCamera"></camera>
  </div>
</template>

<script>
import Camera from './components/Camera.vue'
export default {
  name: 'App',

  data () {
    return {
      showCamera: false
    }
  },

  components: {
    Camera
  }
}
</script>

<style>

  @import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');

  * {
    margin: 0;
    padding: 0;
    font-family: 'VT323', monospace;
  }

  .app {
    width: 100vw;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .main {
    width: 30%;
    height: 35%;
    border: solid 1px rgb(223, 114, 250);
    border-radius: 5px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  h1 {
    font-size: 50px;
  }

  p {
    font-size: 30px;
    margin-bottom: 20px;
  }

  .camera-icon {
    width: 25px;
    height: 25px;
  }

  .camera-icon:hover {
    cursor: pointer;
  }

</style>