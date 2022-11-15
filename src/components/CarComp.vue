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
  <hr />
  <p>Potencias urbanas (menor a 300HP):</p>
  <ul>
    <!-- <li v-for="(power,index) of powers" :key="index">
      <span v-if="power < 300">
        {{power}}
      </span>
    </li> -->
    <template v-for="(power, index) of powers" :key="index">
      <li v-if="power < 300">
        {{ power }}
      </li>
    </template>
  </ul>
  <p>Potencias de carreras (mayores a 300HP):</p>
  <ul>
    <!-- <li v-for="(power,index) of powers" :key="index">
      <span v-if="power >= 300">
        {{power}}
      </span>
    </li> -->
    <template v-for="(power, index) of powers" :key="index">
      <li v-if="power >= 300">
        {{ power }}
      </li>
    </template>
    <hr />
    <h2>Potencias:</h2>
    <ul>
      <template v-for="(power, index) of powers" :key="index">
        <li v-if="power < 280">Urbana: {{power}}HP</li>
        <li v-else-if="power === 280">Híbrida: {{power}}HP</li>
        <li v-else>Carreras: {{power}}HP</li>
      </template>
    </ul>
  </ul>
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
    const powers = [60, 80, 120, 160, 200, 280, 300, 390, 540, 500];
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
      powers,
    };
  },
};
</script>

<style></style>
