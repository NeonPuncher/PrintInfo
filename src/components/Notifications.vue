<template>
    <div class="message-box">
        <h1>{{Noti}}</h1>
        <p class="pProgress">{{NotiText}}</p>
    </div>
</template>

<script>
    export default {
        name: 'Notification',
        props: {
            Noti: String,
            NotiText: String,
        }
    }

</script>

<style>
    .message-box {
        border: solid black;
        border-width: 1px;
        padding: 10px;
        margin: 5px;
    }
</style>