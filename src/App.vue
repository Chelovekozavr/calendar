<template>
  <div id="app">
    <header class="header">
      <div class="header__title-container">
        <img
          src="./assets/OJOWO.svg"
          alt="company logo"
          class="header__title"
        >
        <span class="header__subtitle">
          Beta
        </span>
      </div>
      <div class="header__buttons-container">
        <button class="header__button header__button--notification"></button>
        <button class="header__button header__button--user">Артем</button>
        <button class="header__button header__button--search"></button>
        <button class="header__button header__button--language">Ru</button>

      </div>

    </header>
    <main class="content-container">
      <Navigation />
      <List />
    </main>

  </div>
</template>

<script>
  import Navigation from './components/Navigation';
  import List from './components/List';

  export default {
    name: 'App',

    components: {
      Navigation,
      List
    }
  }
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;700&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=PT+Sans:wght@700&display=swap');

  body {
    margin: 0;
  }

  ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  a {
    color: inherit;
    text-decoration: none;
  }

  button {
    outline: none;
    border: none;
    background: #FFFFFF;
  }

  #app {
    padding: 10px 38px 0;
    text-align: center;
    background-color: #f0f6fc;
    color: #000;
  }

  .header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 48px;

    &__title-container {
    }

    &__title {
      margin-right: 8px;
    }

    &__subtitle {
      font-family: Montserrat, sans-serif;
      font-size: 13px;
      margin-bottom: 50px;
    }

    &__buttons-container {
      display: flex

    }

    &__button {
      display: flex; 
      align-items: center;
      justify-content: center;
      margin-left: 17px;
      padding: 0;

      outline: none;
      border: none;
      background: #FFFFFF;
      box-shadow: 0px 10px 40px rgba(213, 221, 230, 0.6);

      font-family: Montserrat, sans-serif;
      font-weight: 700;
      font-style: 14px;

      &--notification {
        height: 43px;
        width: 43px;
        border-radius: 50%;

        &::after {
          content: "";
          display: block;
          background-image: url("./assets/icons/notification.svg");
          height: 18px;
          width: 18px;
          background-size: 18px 18px;
          background-repeat: no-repeat;
        }
      }

      &--user {
        width:120px;
        height: 43px;
        border-radius: 100px;

        &::after {
          margin-left: 15px;
          content: "";
          display: block;
          background-image: url("./assets/icons/dropDown.svg");
          height: 11px;
          width: 11px;
          background-size: 11px 11px;
          background-repeat: no-repeat;
        }
      }

      &--search {
        height: 43px;
        width: 43px;
        border-radius: 50%;
        background: rgba(203, 215, 228, 0.4);
        box-shadow: none;

        &::after {
          content: "";
          display: block;
          background-image: url("./assets/icons/searchIcon.svg");
          height: 18px;
          width: 18px;
          background-size: 18px 18px;
          background-repeat: no-repeat;
        }
      }

      &--language {
        width: 64px;
        height: 43px;
        border-radius: 100px;
        background: rgba(203, 215, 228, 0.4);
        box-shadow: none;

        &::after {
          margin-left: 8px;
          content: "";
          display: block;
          background-image: url("./assets/icons/dropDown.svg");
          height: 8px;
          width: 8px;
          background-size: 8px 8px;
          background-repeat: no-repeat;
        }
      }
    }

    .content-container {
      display: flex;
      flex-direction: row;
    }
  }
</style>
