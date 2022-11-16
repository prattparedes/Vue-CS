<template lang="">
  <div>
    <h1>VueJS</h1>
    <CarProps :power="power" :upPower="upPower" />
    <!-- <car-comp></car-comp>
    <hr>
    <CarOpt/>
    <hr>
    <CarCom/> -->
  </div>
</template>

<script>
import { ref } from "vue";

import CarProps from "./components/CarProps.vue";
// import CarComp from "./components/CarComp.vue";
// import CarOpt from "./components/CarOpt.vue";
// import CarCom from "./components/CarCom.vue";

export default {
  components: {
    CarProps,
    // CarComp,
    // CarOpt,
    // CarCom,
  },
  setup() {
    let power = ref(45);

    const upPower = () => {
      console.log("aumentar power...");
      power.value++;
      console.log(power);
    };
    return {
      power,
      upPower,
    };
  },
};
</script>
<style lang=""></style>
