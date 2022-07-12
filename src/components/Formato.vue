<template>
  <section class="src-components-formato">
    <div>
      <h1>Ingresar formatos:</h1>
      <p>Ingresar color: <input v-model="myColor" /></p>
      <p>Ingresar fondo: <input v-model="myBackground" /></p>
      <p>Ingresar tamanio: <input v-model="mySize" /></p>
    </div>
    <div>
      <p>
        Ingresar palabra:
        <input
          v-model="myInput"
          :style="{ color: myColor, background: myBackground, fontSize: mySize}"
        />
      </p>
    </div>
    <div>
      <p>Cantidad de palabras: {{ cantidadPalabras }}</p>
    </div>
    <div>
      <table class="table">
        <tr>
          <th>1</th>
          <td>B</td>
        </tr>
        <tr>
          <th>2</th>
          <td>C</td>
        </tr>
        <tr>
          <th>3</th>
          <td>B</td>
        </tr>
        <tr>
          <th>4</th>
          <td>D</td>
        </tr>
        <tr>
          <th>5</th>
          <td>D</td>
        </tr>
      </table>
    </div>
  </section>
</template>

<script>
export default {
  name: "src-components-formato",
  props: [],
  mounted() {},
  data() {
    return {
      myColor: null,
      myBackground: null,
      mySize: null,
      myInput: "",
    };
  },
  methods: {
    dameCantidad() {
      var cant = 0;
      if(this.myInput.split('').length > 0){
        cant = this.myInput.trim().replace(/\s+/gi, ' ').split(" ").length;
      }
      return cant
    },
  },
  computed: {
    cantidadPalabras() {
      return this.dameCantidad();
    },
  },
};
</script>

<style scoped lang="css">
.src-components-formato {
}

</style>
