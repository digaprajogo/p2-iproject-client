<template>
  <div id="app">
    <nav>
      <router-link to="/about">About</router-link> | <router-link to="/home">Home</router-link> |
      <router-link to="/login">Login</router-link> |
      <router-link to="/register">Register</router-link> |
      <router-link to="/maps">Maps</router-link> |
      <router-link to="/markermaps">Marker Maps</router-link> |
      <router-link to="/payment">Payment Page</router-link>
      <!-- <router-link to="/markermapsbyhotel">Marker Maps By Hotel</router-link> -->
    </nav>
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
