<template>
    <div class="progress-box">
        <h2 class="pProgress">{{job}}</h2>
        <p class="pProgress" id="ordernum">Order ID: {{id}}</p>
        <p class="pProgress">
            Priority: {{prio}}<br>
            Filling: {{Fill}}<br>
            Start-time: {{Start}}<br>
            End-time: {{End}}<br>
        </p>
        <h2 class="pProgress">Progress</h2>
        <ProgressBar/>
    </div>
</template>

<script>
    import ProgressBar from './ProgressBar.vue'

    export default {
        name: 'Progress',
        props: {
            job: String,
            id: String,
            prio: String,
            Fill: String,
            Start: String,
            End: String,
        },
        components: {
            ProgressBar
        }
    }
</script>

<style>
    .pProgress {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 1em;
    }

    .progress-box {
        border: solid black;
        border-width: 1px;
        padding: 10px;
        margin: 5px;
    }
</style>