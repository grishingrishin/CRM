<template>
  <div class="tabs">
    <ul class="tabs__list">
      <li class="tabs__item">
        <a href="/" class="tabs__link selected">Вольер 1</a>
      </li>
      <li class="tabs__item">
        <a href="/" class="tabs__link">Вольер 2</a>
      </li>
      <li class="tabs__item">
        <a href="/" class="tabs__link">Вольер 3</a>
      </li>
    </ul>
    <button
      type="button"
      class="tabs__add"
      style="background-image: url(images/add.svg)"
    >
      Добавить вольер
    </button>
  </div>
</template>

<script>
  export default {
    name: "Tabs",
    data() {
      return {

      }
    },
    created() {
      
    },
    mounted() {

    }
  }
</script>

<style>
  .tabs {
    display: flex;
    align-items: center;
  }

  .tabs__list {
    display: flex;
    margin-right: 24px;
    align-items: center;
  }

  .tabs__item {
    position: relative;
    padding: 18px 0;
  }

  .tabs__item:not(:first-child) {
    margin-left: 18px;
  }

  .tabs__link {
    font-size: 16px;
    line-height: 19px;
    color: #D9D9D9;
  }

  .tabs__link.selected {
    color: #484848;
  }

  .tabs__link.selected::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    z-index: 11;
    display: block;
    width: 100%;
    height: 3px;
    background-color: #567354;
    border-radius: 18px;
  }

  .tabs__add {
    width: 20px;
    height: 20px;
    text-indent: -9990px;
    background-color: #D9D9D9;
    background-repeat: no-repeat;
    background-position: center;
    background-size: 10px;
    border-radius: 50%;
    overflow: hidden;
  }
</style>