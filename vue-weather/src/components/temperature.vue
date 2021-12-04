<template>
    <div class="temperature">
        <img src="../../src/assets/thermometer.png">
        <div class="temp-real"> {{ temperature }} </div>
        <div class="temp-feel"> {{ feel }} </div>
    </div>
</template>
<script>
    export default {
        name: "temperature",
        props: ['temperature', 'feel'],
    };
</script>
<style>
    .temperature {
        display: flex;
        align-items: flex-end;
        margin: 15px;
    }
    .temp-real {
        position: relative;
        display: inline-block;
        font-family: "Arial", sans-serif;
        font-size: 100px;
        font-weight: 400;
        color: #fff;
        line-height: 0.9;
        text-shadow: 2px 2px 2px #444;
    }

    .temp-real:after {
        content: "o";
        color: #fff;
        font-size: 35px;
        position: absolute;
        top: -15px;
        right: -25px;
    }

    .temp-feel {
        position: relative;
        box-sizing: border-box;
        padding-right: 15px;
        margin-left: 20px;
        text-align: right;
        text-shadow: 2px 2px 2px #444;
        font-family: "Arial", sans-serif;
        font-size: 30px;
        font-weight: 400;
        color: #eee;
    }

    .temp-feel:before {
        content: "Ощущается";
        display: block;
        position: absolute;
        right: 0;
        top: -17px;
        font-size: 15px;
    }

    .temp-feel:after {
        position: absolute;
        top: -4px;
        right: 2px;
        content: "o";
        font-size: 16px;
        font-weight: 700;
        color: #eee;
    }

    .temperature img {
        width: 70px;
        vertical-align: middle;
    }
</style>
