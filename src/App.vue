<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>

    <div class="wrapper">
      <nav>
        <img class="menu-icon" src="@/assets/svg/burger-icon.svg" alt="" />
        <div class="dropdown">
          <RouterLink to="/"> <img src="" alt="" class="nav-icon home">
            Home</RouterLink>
          <RouterLink to="/about"><img src="" alt="" class="nav-icon about">About me</RouterLink>
          <RouterLink to="/portfolio"><img src="" alt="" class="nav-icon portfolio">Portfolio</RouterLink>
          <RouterLink to="/contact"><img src="" alt="" class="nav-icon contact">Contact me</RouterLink>
        </div>
      </nav>
    </div>
  </header>

  <main>
    <RouterView />
  </main>

</template>

<style lang="scss">
@import '@/assets/base.scss';

body {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  width: 100vw;
  height: 100vh;
  font-family: 'Exo 2', sans-serif;
  position: absolute;

  #app {
    background-color: var(--bg-color);
    background-image: var(--bg-gradient);
    width: 100vw;
    height: 100vh;

    header {
      line-height: 1.5;
      // max-height: 100vh;
      display: flex;
      flex-direction: column;

      .wrapper {


        nav {
          width: 100%;
          font-size: 1rem;
          text-align: center;
          margin-top: 2rem;
          display: flex;
          align-items: center;
          justify-content: center;

          .menu-icon {
            width: 2.5rem;
            height: 2.5rem;
          }

          .dropdown {
            background-color: var(--secondary-color);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;

          }

        }

        nav a.router-link-exact-active {
          color: var(--third-color);
        }

        // nav a.router-link-exact-active:hover {
        //   background-color: var(--third-color);
        // }


        nav a {
          // display: inline-block;
          // padding: 0 1rem;
          // border-left: 1px solid var(--color-border);
          color: var(--dark-color);
          text-decoration: none;
        }

        // nav a:first-of-type {
        //   border: 0;
        // }
      }
    }

    main {
      display: flex;
      flex-direction: column;
      margin: 0;
      padding: 0;
      box-sizing: border-box;


    }
  }
}
</style>
