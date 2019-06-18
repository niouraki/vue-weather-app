<template>
  <div class="home">
    <h1>What's the weather like today?</h1>
    <WeatherNow />
  </div>
</template>

<script>
import WeatherNow from '@/components/weather-now.vue'

export default {
  name: 'home',
  components: {
    WeatherNow
  }
}
</script>

<style>
h1 {
  margin-top: 5vh;
  font-size: 38px;
}
</style>

