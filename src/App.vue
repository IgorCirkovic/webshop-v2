<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view/>
</template>

<style lang="css">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

html, body {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

body {
  background-color: white;
}

#nav {
  padding: 10px;
  width: 100%;
  height: 30px;
  background-color: white;
  line-height: 30px;
}

a {
  font-weight: bold;
  color: gray;
  text-decoration: none;
  margin: 0 5px 0;
  font-size: 1.25rem;

  &.active {
    color: black;
  }
}
</style>
