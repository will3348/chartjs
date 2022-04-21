<template>
  <div class="hello">
    <h1>Hours I Spent on Coding(Last Week)</h1>
    <canvas id="myChart" width="400" height="400"></canvas>
  </div>
</template>

<script>
import Chart from 'chart.js/auto';

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  mounted() {
    console.log('Component mounted.')

    const ctx = document.getElementById('myChart');

    const myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['Mon', 'TUES', 'WED', 'THURS', 'FRI', 'SAT'],
        datasets: [{
            label: '# of HOURS',
            data: [6, 6.5, 7, 6, 4, 2],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            y: {
                beginAtZero: true
            }
        }
    }
});

myChart;
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
