<template>
  <nav class="navigation-container">
    <div class="navigation-top">
      <div class="navigation-top__title">
        <button>
          Эксперт
        </button>
      </div>
      <div class="navigation-top__button">
      </div>
    </div>

    <ul class="navigation-list">
      <li
        class="navigation-list__item"
        v-for="(item) in navigation"
        :key="item.id"
      >
        <img src="@/assets/icons/navigation/1.svg" :alt="item.alt">
        <a href="">{{ item.title }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
  export default {
    data() {
      return {
        navigation: [
          { title: 'Аналитика', id: 1, url: ('@/assets/icons/navigation/analytics.svg'), alt: 'analytics' },
          { title: 'Продукт', id: 2, url: './../assets/icons/navigation/analytics.svg', alt: 'analytics' },
          { title: 'Пользователи', id: 3, url: '../assets/icons/navigation/analytics.svg', alt: 'analytics' },
          { title: 'Конструктор сайта', id: 4, url: '@/assets/icons/navigation/analytics.svg', alt: 'analytics' },
          { title: 'Трансляции', id: 5, url: '../assets/icons/navigation/analytics.svg', alt: 'analytics' },
          { title: 'Рассылка', id: 6, url: '../assets/icons/navigation/analytics.svg', alt: 'analytics' },
          { title: 'Маркетинг', id: 7, url: '../assets/icons/navigation/analytics.svg', alt: 'analytics' },
          { title: 'Платежи', id: 8, url: '../assets/icons/navigation/analytics.svg', alt: 'analytics' },
          { title: 'Настройки', id: 9, url: '../assets/icons/navigation/analytics.svg', alt: 'analytics' }
        ]

      }
    },

  }

</script>

<style lang="scss" scoped>

  .navigation-container {
    width: 250px;
    margin: 0;
  }

  .navigation-top {
    position: relative;
    margin-bottom: 11px;

    &__title {
      position: relative;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 20px;

      width: 157px;
      height: 54px;
      border-radius: 10px;

      font-family: PT Sans, sans-serif;
      font-size: 15px;

      background: #FFFFFF;
      box-shadow: 0px 10px 40px rgba(128, 158, 191, 0.2);
      z-index: 2;

      button {
        font-family: PT Sans, sans-serif;
        font-size: 15px;
      }

      &::after {
        margin-left: 8px;
        content: "";
        display: block;
        background-image: url("../assets/icons/dropDown.svg");
        height: 11px;
        width: 11px;
        background-size: 11px 11px;
        background-repeat: no-repeat;
        z-index: 2;
      }
    }

    &__button {
      position: absolute;
      display: flex;
      justify-content: flex-end;
      padding: 0 20px;
      align-items: center;
      top: 0;
      left: 90px;
      height: 54px;
      width: 124px;
      z-index: 1;

      background: #FFFFFF;
      box-shadow: 0px 10px 40px rgba(128, 158, 191, 0.2);
      border-radius: 10px;

      &::after {
        content: "";
        display: block;
        background-image: url("../assets/icons/bread.svg");
        height: 24px;
        width: 24px;
        background-size: 24px 24px;
        background-repeat: no-repeat;
      }
    }
  }

  .navigation-list {
    width: 177px;
    padding: 10px;

    font-family: PT Sans, sans-serif;
    font-size: 15px;

    background-color: #fff;
    border-radius: 10px;

    box-shadow: 0px 10px 40px rgba(128, 158, 191, 0.2);

    &__item {
      display: flex;
      align-items: center;
      justify-content: center;
      height: 85px;
      border: 1px solid #e7ecf1;
      border-radius: 10px;
      margin-bottom: 10px;
    }
  }

</style>