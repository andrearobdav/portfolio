<template>
  <div class="about">
    <div class="container-glass">
      <h1 class="hello">Sobre Mí</h1>
      <div class="paragraph">
        <p class="text">
          Soy una desarrolladora web Front End que crea proyectos tanto personales como en equipo.
          Además Lorem ipsum dolor, sit amet consectetur adipisicing elit. Qui quas officia amet inventore excepturi
          ipsum
        </p>
        <p class="text">
          alias, rerum, corrupti asperiores labore accusamus aut quisquam voluptate animi soluta quod totam at?
          Adipisci.
          Dolore vitae neque, hic velit eius dolores aperiam, optio, fuga sed magni impedit. Sint soluta quis rem
          corporis
          autem, nihil, ut quae natus dolores ratione necessitatibus doloribus, quam iste quod?
        </p>
      </div>
      <button class="download" type="button">Download CV <img src="../assets/svg/download-icon.svg" alt="download-icon"
          class="download-icon"></button>
      <img src="" alt="Andrea-profile-pic" class="profile-pic">
    </div>
  </div>
</template>

<style lang="scss" scoped>
main {
  .about {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100vw;
    height: 80vh;

    .container-glass {
      width: 90vw;
      display: flex;
      flex-direction: column;
      align-items: center;
      height: 80vh;
      background-color: rgba(255, 255, 255, 0.2);
      border-radius: 25px;
      box-shadow: 2px 2px 15px 5px rgba(0, 0, 0, 0.2);
      -webkit-box-shadow: 2px 2px 15px 5px rgba(0, 0, 0, 0.2);
      border-left: 1px solid #FFFFFF;


      h1 {
        width: 100%;
        color: var(--third-color);
        font-weight: 700;
        font-size: 2.5rem;
        text-align: center;
      }

      .paragraph {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        margin: 0.5rem;

        .text {
          text-align: center;
          font-size: 1rem;
          font-weight: 500;
          color: var(--secondary-color);
        }
      }

      .download {
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 10px;
        background-color: var(--third-color);
        color: var(--secondary-color);
        font-weight: 600;
        font-size: 1rem;
        padding: 0.3rem 0.5rem;
        outline: none;
        border: none;
        cursor: pointer;

        .download-icon {
          width: 2rem;
          height: 2rem;
          padding: 0 0.5rem;
        }
      }
    }
  }
}
</style>
