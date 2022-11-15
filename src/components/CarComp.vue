<template>
  <h2>Coche</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>
    Color:
    <!-- <span v-for="(color, index) in colors" :key="index">
      {{ index }}: {{ color }} -
    </span> -->
  </p>
  <ul>
    <li v-for="(color, index) in colors" :key="index">
      {{ index }}: {{ color }}
    </li>
  </ul>
  <p>Precio: {{ price }}$</p>
  <p>Potencia: {{ power }}HP</p>
  {{ mensaje.title }}
  {{ mensaje.text }}
</template>

<script>
export default {
  // This is OPTIONS API,
  // data() {
  //   return {
  //     brand: "Audi",
  //     model: "A4",
  //     color: ["Azul", "Rojo", "Verde"],
  //     price: 38000,
  //     power: 180,
  //     mensaje: {
  //       title: "Hola mundo",
  //       text: "Adios",
  //     },
  //   };
  // },

  //This is Composition API
  setup() {
    const brand = "Audi";
    const model = "A4";
    const colors = ["Azul", "Morado", "Marrón", "Amarillo"];
    const price = 45000;
    const power = 240;
    const mensaje = {
      title: "Estoy bien",
      text: "Welcome",
    };

    return {
      brand,
      model,
      colors,
      price,
      power,
      mensaje,
    };
  },
};
</script>

<style></style>
