<template>
  <div class="users">
    <div class="users__top">
      <div class="users__tabs">
        <Tabs/>
      </div>
      <div class="users__aside">
        <div class="users__notify">
          <a href="/" class="notify">
            <span
              role="img"
              class="notify__img notify__img_type_inactive"
              style="background-image: url(images/notify.svg)"
              v-if="!notify.isActive"
            >
              У вас нет непрочитанных сообщений
            </span>
            <span
              role="img"
              class="notify__img notify__img_type_active"
              style="background-image: url(images/notify.svg)"
              v-if="notify.isActive"
            >
              У вас есть непрочитанные сообщения
            </span>
          </a>
        </div>
        <div class="users__profile">
          <div class="users__figure">
            <img src="images/ava.png" class="users__ava" alt="Изображение пользователя">
          </div>
          hello@giraffe.com
        </div>
      </div>
    </div>
    <div class="users__headline">
      <h2 class="users__title">
        Жирафы
      </h2>
      <button
        type="button"
        class="users__add"
        style="background-image: url(images/add.svg)"
      >
        Добавить нового пользователя
      </button>
    </div>
    <ul class="users__list">
      <li class="users__item">
        <User/>
      </li>
      <li class="users__item">
        <User/>
      </li>
      <li class="users__item">
        <User/>
      </li>
    </ul>
  </div>
</template>

<script>
  import User from './User.vue';
  import Tabs from './Tabs.vue';

  export default {
    name: "Users",
    components: {
      User,
      Tabs,
    },
    data() {
      return {
        notify: {
          isActive: false
        }
      }
    },
    created() {

    },
    mounted() {

    },
  }
</script>

<style>
  .users {
    height: 100%;
  }

  .users__top {
    position: relative;
    z-index: 1;
    display: flex;
    margin-bottom: 38px;
    align-items: center;
    justify-content: space-between;
  }

  .users__top::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    display: block;
    width: 100%;
    height: 3px;
    background-color: #D9D9D9;
    border-radius: 18px;
  }

  .users__aside {
    display: flex;
    align-items: center;
  }

  .notify__img {
    display: inline-block;
    width: 21px;
    height: 28px;
    text-indent: -999px;
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    overflow: hidden;
  }

  .users__profile {
    display: inline-flex;
    margin-left: 24px;
    align-items: center;
    font-size: 16px;
    line-height: 19px;
    color: #484848;
  }

  .users__figure {
    width: 34px;
    height: 34px;
    margin-right: 14px;
  }

  .users__ava {
    width: 100%;
    height: 100%;
  }

  .users__headline {
    display: flex;
    margin-bottom: 26px;
    align-items: center;
  }

  .users__title {
    margin-right: 14px;
    font-size: 32px;
    line-height: 37px;
    color: #567354;
  }

  .users__add {
    width: 37px;
    height: 37px;
    text-indent: -9999px;
    background-color: #668663;
    background-repeat: no-repeat;
    background-position: center;
    background-size: 16px;
    border-radius: 50%;
    overflow: hidden;
  }

  .users__list {
    display: flex;
    height: inherit;
    margin: 0 -16px;
  }

  .users__item {
    width: 100%;
    max-width: 268px;
    height: 100%;
    max-height: 495px;
    padding: 0 16px;
  }
</style>