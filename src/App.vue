<template>
  <nav>
    <router-link to="/">Home</router-link>
    <router-link to="/about">Sobre</router-link>
    <router-link to="/portfolio">Portfólio</router-link>
    <router-link to="/contact">Contato</router-link>
  </nav>
  <router-view />
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;400;500;600&display=swap");

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-family: "Poppins", sans-serif;
}

nav {
  padding: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 40px;

  a {
    color: #dbdbdb;
    text-decoration: none;
    padding-bottom: 3px;

    &.router-link-exact-active {
      border-bottom: 2px solid #ffbe18;
    }
  }
}
</style>
