<template>
  <div>
    <p>Tu Nombre:</p>
    <input type="text" v-model="nombre"/>

    <p>Ubicación:</p>
    <select v-model="ubicacion">
      <option value="antofagasta">Antofagasta</option>
      <option value="valparaiso">Valparaíso</option>
      <option value="santiago">Santiago</option>
      <option value="concepcion">Concepción</option>
      <option value="valdivia">Valdivia</option>
    </select>

    <p>Lenguaje Favorito:</p>
    <select v-model="lenguaje">
      <option value="javascript">Javascript</option>
      <option value="java">Java</option>
      <option value="python">Python</option>
      <option value="c#">C#</option>
      <option value="swift">Swift</option>
      <option value="ruby">Ruby</option>
    </select>

    <p>Comentarios:</p>
    <textarea v-model="comentarios"></textarea>

    <button>Enviar</button>
  </div>
</template>

<script>
export default {
  name: "Formularios",
  props: {},
  data() {
      return {
        nombre: '',
        ubicacion: '',
        lenguaje: '',
        comentarios: ''
      }     
  }
};
</script>

<style scoped>
    button {
        display: block;
        text-align: center;
    }
</style>