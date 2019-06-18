<template>
  <div id="app">
    <div id="nav">
      <router-link to="/"></router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
html, body {
  min-height: 100vh;
  margin: 0;
  padding: 0;
  background: linear-gradient(to left, #8D909B, #D6EEFF);
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
}
</style>
