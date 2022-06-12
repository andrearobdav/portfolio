<template>
  <div class="container">
    <h1 class="hello">Hola, soy Andrea Robles :)</h1>
    <h2 class="hello">Front End Web Developer</h2>
  </div>
</template>

<style lang="scss" scoped>
main {
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100vw;
    height: 80vh;


    h1 {
      color: var(--secondary-color);
      font-weight: 700;
      font-size: 2.5rem;
      text-align: center;

    }

    h2 {
      color: var(--secondary-color);
      font-weight: 600;
      border: solid 3px #ffffff;
      padding: 0.5rem 1.5rem;
      border-radius: 20px;
    }
  }
}
</style>
