<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">Add news</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #dd5b0f;
}
#nav {
  padding: 50px;
}

#nav a {
  font-weight: bold;
  color: #2b0dd8;
}

#nav a.router-link-exact-active {
  color: #ff0015;
}
</style>
