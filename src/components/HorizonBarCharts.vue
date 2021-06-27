<template>
  <div class="container">
    <div class="Chart">
      <h1 class="pProgress" style="text-align:center;">DownTime</h1>
      <horizontal-bar-example :width="350" :height="250"/>
    </div>
  </div>
</template>

<script>
  import HorizontalBarExample from '../../node_modules/vue-chartjs/src/examples/HorizontalBarExample'

  export default {
    components: {
      HorizontalBarExample
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
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    border-bottom: 1px solid #f1f1f1;
    padding-bottom: 15px;
    font-size: 28px;
    margin-top: 0;
  }

  .Chart {
    padding: 20px;
    border: solid #707070;;
    border-radius: 20px;
    margin: 50px 0;
  }
</style>