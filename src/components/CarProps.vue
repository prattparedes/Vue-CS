<template>
  <h2>Coche</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower">AUMENTAR</button>
  <button @click="downPowerEmit">DISMINUIR</button>
</template>

<script>
export default {
  props: {
    power: {
      type: Number,
      default: 60,
    },
    upPower: Function,

  },

  emits: ["downPower"],

  setup(props, context) {
    const brand = "Audi";
    const model = "A4";

    console.log(context)


    const testPower = () => {
      props.upPower()
    }

    const downPowerEmit = () => {
      context.emit('downPower')
    }

    return {
      brand,
      model,
      testPower,
      downPowerEmit
    };
  },
};
</script>

<style></style>
