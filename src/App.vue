//Dit is de hoofd vue applicatie, dit onderdeel van de App wordt als run path gezien, je kan hier nog steeds werken met templates en andere componenten
//gebruiken door middel van een import functie, ook kunnen hier de style en andere scripts worden toegevoegd.
//Het beste kan je werken met voor iedere component een aparte vue file te maken.

<template>
      <div id="app">
      <NewJob/>
      <PrintInfo/>
  </div>
</template>

<script>
import NewJob from './NewJob.vue'
import PrintInfo from './PrintInfo.vue'

export default {
  name: 'App',
  components: {
    PrintInfo,
    NewJob,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
