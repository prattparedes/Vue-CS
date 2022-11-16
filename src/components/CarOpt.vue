<template>
  <h1>Coche - Options API</h1>
  <p>Marca: {{brand}}</p>
  <p>Modelo: {{model}}</p>
  <p>Potencia: {{power}}HP</p>

  <button @click="upPower(30)">Aumentar</button>
  <button @click="downPower(30)">Disminuir</button>
</template>

<script>
export default {
  data() {
    return {
      brand: "Seat",
      model: "Leon",
      power: 50,
    };
  },
  methods: {
    upPower(newPower) {
        this.power = this.power + newPower
    },
    downPower(newPower) {
        this.power = this.power - newPower
    }
  }
};
</script>

<style></style>
