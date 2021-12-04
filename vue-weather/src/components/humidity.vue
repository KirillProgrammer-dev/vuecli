<template>
    <div class="humidity">
        <img src="../../src/assets/humidity.png"> {{ humidity }} <small>%</small>
    </div>
</template>
<script>
    export default {
        name: "humidity",
        props: ['humidity'],
        data() {
            return {};
        }
    };
</script>
<style>
    .humidity {
        display: inline-block;
        position: relative;
        margin: 15px;
        text-shadow: 2px 2px 2px #444;
        font-family: "Arial", sans-serif;
        font-size: 40px;
        font-weight: 400;
        color: #fff;
        line-height: 0.9;
    }

    .humidity small {
        font-size: 30px;
        margin-left: -5px;
    }

    .humidity img {
        width: 30px;
        margin-right: -10px;
        vertical-align: middle;
    }
</style>
