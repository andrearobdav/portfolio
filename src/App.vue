<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref } from "vue";

const best_dropdown = ref(localStorage.getItem("best_dropwdown") === "true");
const isOpen = () => {
  best_dropdown.value = !best_dropdown.value;
  localStorage.setItem("best_dropdown", best_dropdown.value);
};

</script>

<template>
  <header>

    <!-- <div :class="`${best_dropdown ? 'best-dropdown' : ''}`"> -->
    <nav :class="`${best_dropdown ? 'best-dropdown' : ''}`">
      <button class="toggle-prof" v-on:click="isOpen">
        <img class="menu-icon" src="@/assets/svg/burger-icon.svg" alt="" />
      </button>
      <div class="dropdown-content" id="myDropdown">
        <RouterLink to="/"> <img src="" alt="" class="nav-icon home">
          Home</RouterLink>
        <RouterLink to="/about"><img src="" alt="" class="nav-icon about">About me</RouterLink>
        <RouterLink to="/portfolio"><img src="" alt="" class="nav-icon portfolio">Portfolio</RouterLink>
        <RouterLink to="/contact"><img src="" alt="" class="nav-icon contact">Contact me</RouterLink>
      </div>
    </nav>
    <!-- </div> -->
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


      // & .best-dropdown {
      //   width: 100%;
      //   font-size: 1rem;
      //   text-align: center;
      //   margin-top: 2rem;
      //   display: flex;
      //   align-items: center;
      //   justify-content: center;
      & nav {
        display: flex;
        align-items: center;
        justify-content: center;
        height: 5rem;

        .toggle-prof {
          display: flex;
          align-items: center;
          justify-content: center;
          outline: none;
          border: none;
          background-color: transparent;

          .menu-icon {
            width: 2.5rem;
            height: 2.5rem;
          }
        }

        .dropdown-content {
          display: none;

          .router-link {
            display: none;
          }

        }
      }

      & .best-dropdown {
        width: 100%;
        font-size: 1rem;
        text-align: center;
        margin-top: 2rem;
        display: flex;
        align-items: center;
        justify-content: center;

        .toggle-prof {
          display: flex;
          align-items: center;
          justify-content: center;
          width: 4rem;
          height: 4rem;
          outline: none;
          border: none;

          .menu-icon {
            width: 2.5rem;
            height: 2.5rem;
          }
        }

        .dropdown-content {
          display: block;
          position: relative;
          display: flex;
          flex-direction: column;
          justify-content: space-around;
          align-items: center;
          background-color: white;
          box-shadow: 2px 2px 15px 5px rgba(0, 0, 0, 0.2);
          -webkit-box-shadow: 2px 2px 15px 5px rgba(0, 0, 0, 0.2);
          width: 14rem;
          height: 12rem;
          padding: 1rem;
          transition: 0.3s ease-out;

          .router-link {
            display: block;
            position: fixed;
            color: #282828;
            text-decoration: none;
            font-weight: 500;
            display: flex;
            align-items: center;
            flex-direction: row;
            cursor: pointer;

          }
        }
      }

      nav a.router-link-exact-active {
        color: var(--third-color);
      }

      // nav a.router-link-exact-active:hover {
      //   background-color: var(--third-color);
      // }


      nav a {
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
</style>
