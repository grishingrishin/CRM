<template>
  <div class="profile">
    <figure class="profile__figure">
      <img :src="figure.src" class="profile__ava" alt="Картинка пользователя">
    </figure>
    <div class="profile__info">
      <b class="profile__name">
        {{ name }}
      </b>
      {{ info }}
    </div>
  </div>
</template>

<script>
  export default {
    name: "profile",
    data() {
      return {
        figure: {
          src: "images/ava.png"
        },
        name: "Ферма Заслуженных Жирафов",
        info: "России и СНГ",
      }
    },
    created() {

    },
    mounted() {

    }
  }
</script>

<style>
  .profile {
    display: flex;
    margin-bottom: 54px;
    align-items: center;
    font-size: 10px;
    line-height: 12px;
  }

  .profile__figure {
    flex: 0 0 auto;
    width: 59px;
    height: 59px;
    margin-right: 8px;
    border-radius: 50%;
    overflow: hidden;
  }

  .profile__name {
    display: block;
    margin-bottom: 6px;
  }
</style>