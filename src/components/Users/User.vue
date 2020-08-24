<template>
  <article class="user">
    <div class="user__actions">
      <div class="user__settings settings">
        <button 
          type="button"
          class="settings__dropdown"
          style="background-image: url(images/dropdown.svg)"
          @click="settings.isOpen = !settings.isOpen"
        >
          Настройки
        </button>
        <ul class="settings__list" v-show="settings.isOpen">
          <li class="settings__item">
            <a href="/" class="settings__link">
              <span
                role="img"
                class="settings__icon"
                style="background-image: url(images/settings_edit.svg)"
                aria-label="Иконка редактирования"
              ></span>
              Редактировать
            </a>
          </li>
          <li class="settings__item">
            <a href="/" class="settings__link">
              <span
                role="img"
                class="settings__icon"
                style="background-image: url(images/settings_del.svg)"
                aria-label="Иконка удаления"
              ></span>
              Удалить
            </a>
          </li>
        </ul>
      </div>
    </div>
    <figure class="user__figure">
      <img src="images/user.png" alt="Изображение пользователя" class="user__ava">
    </figure>
    <h3 class="user__name">Гога</h3>
    <div class="user__data">
      <table class="user__table">
        <tr class="user__row">
          <td class="user__cell">
            <img src="images/table_1.svg" alt="Пол">
          </td>
          <td class="user__cell">
            <img src="images/table_2.svg" alt="Вес">
          </td>
          <td class="user__cell">
            <img src="images/table_3.svg" alt="Рост">
          </td>
        </tr>
        <tr class="user__row">
          <td class="user__cell">
            Ж
          </td>
          <td class="user__cell">
            800
          </td>
          <td class="user__cell">
            4
          </td>
        </tr>
      </table>
    </div>
    <ul class="user__list">
      <li class="user__item">
        <span class="user__spec">Цвет:</span>
        Стандарт
      </li>
      <li class="user__item">
        <span class="user__spec">Диета:</span>
        Растительная
      </li>
      <li class="user__item">
        <span class="user__spec">Характер:</span>
        Кокетка
      </li>
    </ul>
  </article>
</template>

<script>
  export default {
    name: "User",
    data() {
      return {
        settings: {
          isOpen: false,
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
  .user {
    height: 100%;
    padding: 14px 32px 38px;
    color: #435F40;
    background-color: #F3DBC7;
    border-radius: 24px;
  }

  .user__actions {
    display: flex;
    align-items: center;
    justify-content: flex-end;
  }

  .settings {
    position: relative;
  }

  .settings__dropdown {
    width: 18px;
    height: 21px;
    text-indent: -9999px;
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
  }

  .settings__list {
    position: absolute;
    left: 0;
    z-index: 99;
    width: 174px;
    padding: 14px 10px;
    color: #fff;
    background-color: #668663;
    border-radius: 20px;
  }

  .settings__item:not(:last-child) {
    margin-bottom: 6px;
  }

  .settings__link {
    display: flex;
    padding: 6px 14px 8px;
    align-items: center;
    font-size: 14px;
    line-height: 16px;
    border-radius: 52px;
  }

  .settings__link:hover {
    background-color: #567354;
  }

  .settings__icon {
    display: inline-block;
    width: 16px;
    height: 18px;
    margin-right: 8px;
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
  }

  .user__ava {
    display: block;
    width: 145px;
    height: 145px;
    margin: 0 auto;
    overflow: hidden;
    object-fit: cover;
  }

  .user__name {
    margin: 28px 0;
    text-align: center;
    font-weight: 500;
    font-size: 22px;
    line-height: 26px;
  }

  .user__table {
    position: relative;
    z-index: 1;
    width: 100%;
    table-layout: fixed;
    border-collapse: collapse;
  }

  .user__table::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: -6%;
    z-index: -1;
    display: block;
    width: 112%;
    height: 39px;
    background-color: #DCB18B;
    border-radius: 58px;
  }

  .user__row {
    height: 39px;
  }

  .user__cell {
    text-align: center;
    vertical-align: middle;
    font-weight: 500;
  }

  .user__row:nth-child(even) .user__cell {
    color: #333; 
  }

  .user__data {
    margin-bottom: 22px;
  }

  .user__item {
    font-size: 16px;
    line-height: 19px;
  }

  .user__item:not(:last-child) {
    margin-bottom: 18px;
  }

  .user__spec {
    font-weight: 500;
  }
</style>