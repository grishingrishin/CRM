<template>
  <nav class="navbar">
    <ul class="navbar__nav nav">
      <li class="nav__item" v-for="(item, index) in items" :key="index">
        <a :href="item.path" :class="['nav__link', { selected: index === 2 ? true : false }]">
          <span
            role="img"
            class="nav__icon"
            :style="{ backgroundImage: `url('${item.icon}')` }"
            :aria-label="`Иконка пункта ${item.name.toLowerCase()}`"
          ></span>
          {{ item.name }}
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
  export default {
    name: "MainNavbar",
    data() {
      return {
        items: [
          {
            icon: "images/1.svg",
            name: "Главная",
            path: "/"
          },
          {
            icon: "images/2.svg",
            name: "Управление",
            path: "/"
          },
          {
            icon: "images/3.svg",
            name: "Жирафы",
            path: "/"
          },
          {
            icon: "images/4.svg",
            name: "Сотрудники",
            path: "/"
          },
          {
            icon: "images/5.svg",
            name: "Настройки",
            path: "/"
          },
          {
            icon: "images/6.svg",
            name: "Поддержка",
            path: "/"
          },
        ]
      }
    },
    created() {

    },
    mounted() {

    },
  }
</script>

<style>
  .nav__item:not(:last-child) {
    margin-bottom: 28px;
  }

  .nav__link {
    display: flex;
    padding: 11px 18px 12px;
    align-items: center;
    font-size: 16px;
    line-height: 22px;
    background-color: #567354;
    border-radius: 24px;
  }

  .nav__link.selected {
    font-weight: 500;
    color: #567354;
    background-color: #fff;
  }

  .nav__icon {
    display: inline-block;
    width: 24px;
    height: 28px;
    margin-right: 1.5em;
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
  }
</style>