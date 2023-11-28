<template>
  <div id="app">
    <survey :survey="survey" />
  </div>
</template>

<script>
import "survey-core/defaultV2.css";
import { Model } from "survey-core";
import { Survey } from "survey-vue-ui";

export default {
  name: "App",
  components: {
    Survey
  },
  data() {
    return {
      survey: new Model({
        title: "Encuesta de Prueba",
        questions: [
          {
            type: "text",
            name: "nombre",
            title: "¿Cuál es tu nombre?"
          },
          // Agrega más preguntas aquí
        ]
      })
    };
  }
};
</script>

<style>
/* Estilos personalizados aquí */
</style>
