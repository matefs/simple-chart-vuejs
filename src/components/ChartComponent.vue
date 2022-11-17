<script setup  >
import Chart from 'chart.js/auto';
import { ref, onMounted } from 'vue'

function log(variable){
    return console.log(variable)
}


onMounted(() => {
    log('Chart Mounted')
    const data = [
    { year: 2010, count: 10 },
    { year: 2011, count: 20 },
    { year: 2012, count: 15 },
    { year: 2013, count: 25 },
    { year: 2014, count: 22 },
    { year: 2015, count: 30 },
    { year: 2016, count: 28 },  
    ];
    
     

    
  new Chart(
    document.getElementById('myChart'),
    {
      type: 'line',
      data: {
        labels: data.map(row => row.year),
        datasets: [
          {
            label: 'Acquisitions by year',
            data: data.map(row => row.count),
            borderColor: '#3498db'

          }, 
                  ]
      }
    }
  );


})


</script>
<template>
    <h2>My chart</h2>
    <div>
        <canvas id="myChart" ></canvas> 
    </div>

</template>
<style scoped>
 #myChart{
  width: 80vh;
}

</style>