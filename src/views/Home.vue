<template>
  <div class="home">
    <predict-plot-grid :points="points" :descriptions="descriptions"/>
  </div>
</template>

<script>
// @ is an alias to /src
import { points } from "@/assets/2dArray.js";
import { values } from "@/assets/descriptions.js";

import PredictPlotGrid from "@/components/PredictPlotGrid/PredictPlotGrid.vue";

export default {
  name: "home",
  components: {
    PredictPlotGrid
  },
  data() {
    return {
      points: null,
      descriptions: null
    };
  },
  mounted() {
    this.points = points;
    this.descriptions = values;
  }
};
</script>
