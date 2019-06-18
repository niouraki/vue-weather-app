<template>
  <div class="weather-now">
      <h2>Location</h2>
      <p>{{ location }}</p>
      <table>
          <tr>
              <th>Wind</th>
              <th>Temperature</th>
              <th>Humidity</th>
          </tr>
          <tr>
              <td>TBD</td>
              <td>TBD</td>
              <td>TBD</td>
          </tr>
      </table>
      <input type="text" placeholder="Enter Location" v-model="location" v-on:keyup.enter="submit">
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'weather-now',
  data () {
      return {
          location: ""
      }
  },
  methods: {
      submit () {
          console.log(this.location)
          axios.get(`https://api.mapbox.com/geocoding/v5/mapbox.places/${this.location}.json?access_token=pk.eyJ1IjoibmlvdXJha2kiLCJhIjoiY2p4MjJnNGswMDE5ajQ0bzN6YTRwc3dmbyJ9.n1Ls6E9BAho3pfZ19Zs47Q&autocomplete=true`)
            .then(response => console.log(response))
      }
  }
}
</script>

<style>
.weather-now {
    position: relative;
    border: 2px solid black;
    width: 60vw;
    height: 60vh;
    text-align: center;
    margin: 10vh auto;
    box-shadow: -21px 18px 17px -18px rgba(0,0,0,0.75);
    border-radius: 5px;
    background: linear-gradient(to bottom, black 20%, white 20% 100%);
}

table {
    margin: 10vh auto;
    
    width: 80%;
}

table th {
    font-size: 20px;
}

table td {
    font-size: 18px;
}

input {
    display: inline-block;
    margin: 3vh auto;
    width: 80%;
    font-size: 18px;
}

h2 {
    margin-top: 15vh;
}
</style>

