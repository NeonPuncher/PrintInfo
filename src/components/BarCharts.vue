<template>
  <div class="container">
    <div class="Chart">
      <h1 class="pProgress" style="text-align:center;">DownTime</h1>
      <bar-example :width="350" :height="250"/>
    </div>
  </div>
</template>

<script>
  import BarExample from '../../node_modules/vue-chartjs/src/examples/BarExample'

  export default {
    components: {
      BarExample
    },
    mounted () {}
  }
</script>

<style>
  .container {
    float: left;
    margin: 20px;
  }

  h1 {
    border-bottom: 1px solid #f1f1f1;
    padding-bottom: 15px;
    font-size: 28px;
    margin-top: 0;
  }

  .Chart {
    padding: 20px;
    border-radius: 20px;
    margin: 50px 0;
  }
</style>