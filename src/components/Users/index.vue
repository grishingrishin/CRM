<template>
  <div class="users">
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

  export default {
    name: "Users",
    components: {
      User
    },
    data() {
      return {

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