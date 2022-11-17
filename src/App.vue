<script setup  > 
import ChartComponent from './components/ChartComponent.vue';  
import { ref } from 'vue'
var showChartVariable = ref(false); 
 
 

</script>

<template>
<main>

<button @click="showChartVariable = !showChartVariable"> Display chart </button>

<div v-if="showChartVariable" > 
  <ChartComponent /> 
</div>
<div v-else>
  Try to see the charts
</div>

  </main> 
</template>
 