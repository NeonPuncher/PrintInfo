<template>
  <div class="container">
    <div class="Chart">
      <h1 class="pProgress" style="text-align:center;">DownTime</h1>
      <line-example :width="350" :height="250"/>
    </div>
  </div>
</template>

<script>
  import LineExample from '../../node_modules/vue-chartjs/src/examples/LineExample'

  export default {
    components: {
      LineExample
    },
    mounted () {}
  }
</script>
