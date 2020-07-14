<template>
  <div id="app" class="background">
    <div class="container">
      <h2>ENCUESTA DEL DOJO</h2>
      <Formularios />
    </div>
  </div>
</template>

<script>
import Formularios from "./components/Formularios.vue";

export default {
  name: "App",
  components: {
    Formularios
  },
  data: () => {
    return {};
  }
};
</script>

<style lang='scss'>

@import "~vue-material/dist/theme/engine"; // Import the theme engine

@include md-register-theme("default", (
  primary: #80ffc3, // The primary color of your application
  accent: #964ee9, // The accent or secondary color
  theme: dark // This can be dark or light
));

@import "~vue-material/dist/components/MdList/theme"; // Apply the Button theme
@import "~vue-material/dist/components/MdButton/theme"; // Apply the Button theme
@import "~vue-material/dist/components/MdField/theme"; // Apply the Button theme
@import "~vue-material/dist/components/MdRadio/theme"; // Apply the Button theme
@import "~vue-material/dist/components/MdDialog/theme"; // Apply the Button theme

body {
  margin: 0 !important;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.background {
  position: absolute;
  height: 100%;
  width: 100%;
  overflow: auto;
  background: linear-gradient(to top, #240422, #007e8a) fixed;
}
.container {
  background-color: rgba(12, 12, 12, 0.15);
  border-radius: 5px;
  padding: 25px;
  padding-bottom: 5px;
  margin: 0.5rem auto;
  overflow: hidden;
  backdrop-filter: blur(5px);
  max-width: 310px;
  position: absolute;
  left: 0;
  right: 0;
  color: #ffffff;
}
h2 {
  text-align: center;
}
.md-list.md-theme-default {
  background-color: #381a37f3;
}
.md-dialog-container.md-theme-default {
  background-color: #381a37f3;
  color: #fff;
}
</style>
