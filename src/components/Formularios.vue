<template>
  <div>
    <md-field>
      <label>Nombre</label>
      <md-input type="text" v-model="nombre" />
    </md-field>

    <md-field>
      <label>Edad</label>
      <md-input type="number" v-model="edad" />
    </md-field>

    <md-field>
      <label>Ubicación</label>
      <md-select v-model="ubicacion">
        <md-option value="Antofagasta">Antofagasta</md-option>
        <md-option value="Valparaíso">Valparaíso</md-option>
        <md-option value="Santiago">Santiago</md-option>
        <md-option value="Concepción">Concepción</md-option>
        <md-option value="Valdivia">Valdivia</md-option>
      </md-select>
    </md-field>

    <md-field>
      <label>Lenguaje Favorito</label>
      <md-select v-model="lenguaje">
        <md-option value="JavaScript">JavaScript</md-option>
        <md-option value="Java">Java</md-option>
        <md-option value="Python">Python</md-option>
        <md-option value="C#">C#</md-option>
        <md-option value="Swift">Swift</md-option>
        <md-option value="Ruby">Ruby</md-option>
      </md-select>
    </md-field>

    <div>
      <label class="genero">Género</label>

      <md-radio v-model="genero" value="Femenino" class="md-primary">Femenino</md-radio>
      <md-radio v-model="genero" value="Masculino" class="md-primary">Masculino</md-radio>
      <md-radio v-model="genero" value="Otro" class="md-primary">Otro</md-radio>
    </div>

    <md-field class="comentarios">
      <label>Comentarios</label>
      <md-textarea v-model="comentarios"></md-textarea>
    </md-field>

    <md-dialog-alert
      :md-active.sync="modal"
      md-title="Tus Respuestas:"
      :md-content="'Nombre: ' + nombre + '<br>Edad: ' + edad + '<br>Ubicación: ' + ubicacion + '<br>Lenguaje Favorito: ' + lenguaje + '<br>Género: ' + genero + '<br>Comentarios: ' + comentarios"
    />
    <md-button class="md-raised" @click="modal = true">Enviar</md-button>
  </div>
</template>

<script>
export default {
  name: "Formularios",
  props: {},
  data() {
    return {
      nombre: "",
      ubicacion: "",
      edad: "",
      genero: "",
      lenguaje: "",
      comentarios: "",
      modal: false
    };
  }
};
</script>

<style scoped>
.md-button.md-theme-default.md-raised:not([disabled]) {
  background-color: #5f015ab0;
}
.md-field.md-has-textarea:not(.md-autogrow) .md-textarea {
  min-height: 3rem;
  resize: none;
}
.genero {
  position: relative;
  display: block;
  text-align: left;
  font-size: 16px;
  line-height: 20px;
  color: rgba(255, 255, 255, 0.7);
}
.md-radio {
  display: flex;
}
.comentarios {
  top: 10px;
}
</style>