//Dit is de hoofd vue applicatie, dit onderdeel van de App wordt als run path gezien, je kan hier nog steeds werken met templates en andere componenten
//gebruiken door middel van een import functie, ook kunnen hier de style en andere scripts worden toegevoegd.
//Het beste kan je werken met voor iedere component een aparte vue file te maken.

<template>
    <modal class="Modal" btnText="Open Print Info">
    <div class="PrintInfo">
      <div class="header">
        <h1 style="float:left">Printer Info</h1>
        <h1 style="float:right">X</h1>
      </div>
      <div class="Progress-Box">
        <h1>Print Progress</h1>
        <Progress job="Job 1" id="12" prio="High" fill="59%" start="12-12-2021" end="03-04-2022"/>
        <Progress job="Job 2" id="315" prio="Low" fill="87%" start="28-11-2021" end="29-12-2021"/>
        <Progress job="Job 3" id="981" prio="Medium" fill="39%" start="09-12-2021" end="01-09-2022"/>
      </div>
      <div class="Error-Box">
        <h1>Logs:</h1>
        <Notifications Noti="Completed" NotiText="- Er waren geen Errors, alles is fijnloos afgerond."/>
        <Notifications Noti="Error" NotiText="- De staalpoeder moet worden aangevuld"/>
      </div>
      <div class="Chart-container">
        <div>
          <BarCharts/>
          <LineCharts/>
          <HorizonBarCharts/>
        </div>
      </div>
    </div>
    </modal>
</template>

<script>
import BarCharts from './components/BarCharts.vue'
import LineCharts from './components/LineCharts.vue'
import HorizonBarCharts from './components/HorizonBarCharts.vue'
import Notifications from './components/Notifications.vue'
import Progress from './components/Progress.vue'
import Modal from "@melmacaluso/vue-modal";

export default {
  name: 'PrintInfo',
  components: {
    BarCharts,
    LineCharts,
    HorizonBarCharts,
    Notifications,
    Progress,
    Modal,
  }
}
</script>

<style>
.PrintInfo {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: white;
  width: 70%;
  height: 60%;
}

.header {
  height: 30px;
  width: 100%;
  padding: 1%;
  float: left;
  background-color: #151539;
  color: rgb(255, 255, 255);
}

.Chart-container {
    float: left;
    width: 100%;
    border: solid black;
    background-color: white;
    border-width: 3px;
    padding: 5px;
}

.Progress-Box {
  width: 49%;
  float: left;
  height: 350px;
  border: solid black;
  background-color: white;
  border-width: 3px;
  padding: 5px;
  overflow-y: scroll;
}

.Error-Box {
  width: 48%;
  height: 350px;
  float: left;
  border: solid black;
  background-color: white;
  border-width: 3px;
  padding: 5px;
  overflow-y: scroll;
}

</style>
