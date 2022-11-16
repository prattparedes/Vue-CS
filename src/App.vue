<template lang="">
  <div>
    <h1>VueJS</h1>
    <car-comp></car-comp>
    <hr>
    <CarOpt/>
    <hr>
    <CarCom/>
  </div>
</template>

<script>
import CarComp from "./components/CarComp.vue";
import CarOpt from "./components/CarOpt.vue";
import CarCom from "./components/CarCom.vue";

export default {
  components: {
    CarComp,
    CarOpt,
    CarCom,
  },
};
</script>
<style lang=""></style>
