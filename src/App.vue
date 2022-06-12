<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>

    <div class="wrapper">

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About me</RouterLink>
        <RouterLink to="/portfolio">Portfolio</RouterLink>
        <RouterLink to="/contact">Contact me</RouterLink>
      </nav>
    </div>
  </header>


  <RouterView />


</template>

<style lang="scss">
@import '@/assets/base.scss';

#app {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: 'Exo 2', sans-serif;
  background-color: var(--bg-color);
  background-image: var(--bg-gradient);
  width: 100vw;
  height: 100vh;


  header {
    line-height: 1.5;
    // max-height: 100vh;
    display: flex;
    flex-direction: column;

    nav {
      width: 100%;
      font-size: 1rem;
      text-align: center;
      margin-top: 2rem;

    }

    nav a.router-link-exact-active {
      color: var(--third-color);
    }

    nav a.router-link-exact-active:hover {
      background-color: var(--third-color);
    }


    nav a {
      // display: inline-block;
      padding: 0 1rem;
      border-left: 1px solid var(--color-border);
      color: var(--secondary-color);
      text-decoration: none;
    }

    nav a:first-of-type {
      border: 0;
    }
  }

  body {
    display: flex;
    flex-direction: column;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: var(--bg-color);
    background-image: var(--bg-gradient);
    width: 100vw;
    height: 100vh;

  }
}
</style>
