<template>
  <b-container id="app">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/arquivo-retorno">Arquivo de Retorno</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view/>
  </b-container>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100%;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
