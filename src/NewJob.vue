<template>
    <Modal class="Modal" btnText="Create New Job">
    <div class="Job-box">
        <div class="header">
            <h1 style="float:left">Create a new Job</h1>
            <h1 style="float:right">X</h1>
        </div>
        <div class="Job-info">
            <h2>Job Info</h2>
            <div style="margin-bottom:20px">
            <label>Job Name</label>
            <input class="inputfield" placeholder="Order-number" type="text" maxlength="14" size="14">
            </div>
            <div style="margin-bottom:20px">
            <label>Start Date</label>
            <input class="inputfield" placeholder="--/--/----" type="text" maxlength="10" size="10">
            </div>
            <div style="margin-bottom:20px">
            <label>Due Date</label>
            <input class="inputfield" placeholder="Calculating" type="text" maxlength="8" size="8">
            </div>
        </div>
        <div class="Print-info">
            <h2 style="">Print Info</h2>
            <div style="margin-bottom:20px">
            <label>File upload</label>
            <input class="inputfield" placeholder="Select File" type="text" maxlength="10" size="10">
            </div>
            <div style="margin-bottom:20px">
            <label>Priority</label>
            <select class="inputfield">
                <option value="High">High</option>
                <option value="Medium">Medium</option>
                <option value="Low">Low</option>
            </select>
            </div>
            <div style="margin-bottom:20px">
            <label>Material</label>
            <select class="inputfield">
                <option value="Steel">Steel</option>
                <option value="Aluminium">Aluminium</option>
                <option value="Carbon">Carbon</option>
                <option value="Iron">Iron</option>
            </select>
            </div>
        </div>
        <div class="Available-print">
            <h2 style="margin-left: 26px">Available Printers</h2>
            <div class="Print-box">
                <h3>Machine 1</h3>
                <button class="JobButton">Job 1</button>
                <button class="JobButton">Job 2</button>
                <button class="JobButton">Job 3</button>
                <p>Due data: 15 May - 11:00</p>
                <h4 style="float:right; margin-top:-5px">First Available</h4>
            </div>
            <div class="Print-box">
                <h3>Machine 2</h3>
                <button class="JobButton">Job 1</button>
                <button class="JobButton">Job 2</button>
                <button class="JobButton">Job 3</button>
                <p>Due data: 15 May - 19:00</p>
                <h4 style="float:right; margin-top:-5px">_</h4>
            </div>
            <div class="Print-box">
                <h3>Machine 2</h3>
                <button class="JobButton">Job 1</button>
                <button class="JobButton">Job 2</button>
                <button class="JobButton">Job 3</button>
                <p>Due data: 15 May - 19:00</p>
                <h4 style="float:right; margin-top:-5px">_</h4>
            </div>
        </div>
        <button class="Create-Button">Create Job</button>
    </div>
    </Modal>
</template>

<script>
import Modal from "@melmacaluso/vue-modal";

export default {
    name: 'NewJob',
    components: {
        Modal,
    }
}

</script>

<style>
    h2 {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        color: #707070;
        font-size: 2em;
    }

    p {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        color: #707070;
        font-size: 0.7em;
    }

    h4 {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        color: #2B2B67;
        font-size: 0.7em;
    }

    label {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        color: #707070;
        font-size: 2em;
        display: inline-block;
        width: 160px;
        text-align: left;
    }

    .Job-box {
        width: 70%;
        height: 850px;
        margin-top: 2%;
        margin-left: 15%;
        background: white;
        box-shadow: 0px 0px 20px 2px rgba(0, 0, 0, .4);
    }

    .header {
        height: 8%;
        padding: 1%;
        background-color: #151539;
        color: white;
    }

    .Job-info {
        width: 47.95%;
        height: 36%;
        float: left;
        padding-left: 26px;
        border-color: #707070;
        border-width: 1px;
    }

    .Print-info {
        width: 47.95%;
        height: 36%;
        float: left;
        padding-left: 26px;
        border-color: #707070;
        border-width: 1px;
    }

    .Available-print {
        width: 100%;
        height: 50%;
    }

    .Print-box {
        float: left;
        font-size: 30px;
        width: 330px;
        height: 60%;
        border-radius: 19px;
        border-color: #707070;
        border-width: 1px;
        margin-left: 3%;
        padding: 19px;
        box-shadow: 0px 0px 20px 2px rgba(0, 0, 0, .4);
    }

    .inputfield {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        height: 40px;
        padding-left: 14px;
        margin-left: 26px;
        border-radius: 11px;
        font-size: 25px;
    }

    .JobButton {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 25px;
        width: 100px;
        text-align: center;
        margin: 5px;
        background-color: transparent;
        border-radius: 14px;
        border-color: #707070;
        border-width: 1px;
        color: #707070;
    }

    .JobButton:hover {
        background-color: #E4E4E4;
        color: #262626;
    }

    .JobButton:focus {
        background-color: #2B2B67;
        color: white;
    }

    button {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 30px;
        padding: 10px;
        margin: 26px;
        border-radius: 20px;
        background-color: #2B2B67;
        color: white;
    }

    button:hover {
        background-color: #0b0b33;
    }
</style>