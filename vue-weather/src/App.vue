<template>
  <div class="app">
    <div class="informer-container">
      <temperature :temperature="temperatureReal" :feel="temperatureFeel"></temperature>
      <div class="flex-break"></div>
      <humidity :humidity="humidity"></humidity>
      <div class="vertical-divider"></div>
      <wind :wind="wind"></wind>
    </div>
  </div>
</template>

<script>
import humidity from "./components/humidity.vue";
import temperature from "./components/temperature.vue";
import wind from "./components/wind.vue";

export default {
  name: "body",
  data() {
    return {
      temperatureReal: "1",
      temperatureFeel: '-3.2',
      humidity: "6",
      wind: "20",
    }
  },
  components: {
    humidity,
    temperature,
    wind
  }
};
</script>

<style>
  body {
    margin: 0;
    padding: 0;
  }

  .app {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background: rgb(244, 123, 186);
    background: linear-gradient(
      -25deg,
      rgba(244, 123, 186, 0.5) 20%,
      rgba(90, 95, 245, 0.5) 80%
    );
  }

  .informer-container {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    flex-wrap: wrap;
    width: 400px;
    padding: 30px;
    background-image: url("../src/assets/forest.png");
    background-size: cover;
    background-position: center center;
    border-radius: 20px;
    box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.75);
  }

  .flex-break {
    flex-basis: 100%;
    height: 0;
  }

  .vertical-divider {
    height: 70px;
    width: 1px;
    background-color: #fff;
    vertical-align: middle;
    display: table-cell;
  }
</style>
