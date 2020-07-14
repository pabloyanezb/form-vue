<template>
  <div id="app" class="background">
    <div class="container">
      <h2>
        Encuesta del Dojo
      </h2>
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
    return {
      
    };
  }
};
</script>

<style>
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
  background: linear-gradient(to top, #360033, #0b8793);
}
.container {
  background-color: rgba(53, 53, 53, 0.102);
  border-radius: 10px;
  padding: 25px;
  margin-top: 3rem;
  backdrop-filter: blur(5px);
  box-shadow: -7px -7px 23px -4px rgba(0, 0, 0, 0.2);
  max-width: 280px;
  position: absolute;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  color: #e8f9ff;
}
h2 {
  margin-bottom: 2rem;
  text-align: center;
}
</style>
