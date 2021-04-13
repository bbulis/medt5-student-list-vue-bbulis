<template>
  <div id="app">
<!--    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>-->
    <div class="header">
      <h1>Schüler Liste</h1>
      <p>Schuljahr 2020/21</p>
    </div>
    <div class="container_own">
      <router-view />
    </div>
  </div>
</template>

<style>
#app {
  font-family: "Roboto", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.container_own {
  width: 50%;
  margin: 0 auto;
}

.header {
  text-align: center;
  padding: 10px;
  background: #44b78b;
  color: white;
  font-size: 40px;
}

h1 {
  font-size: 60px !important;
}
</style>
