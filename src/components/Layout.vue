<template>
  <div class="wrapper">
    <div class="sidebar">
      <div class="sidebar__profile">
        <Profile/>
      </div>
      <div class="sidebar__nav">
        <MainNavbar/>
      </div>
    </div>
    <div class="main">
      <slot></slot>
    </div>
  </div>
</template>

<script>
  import Profile from './Profile.vue';
  import MainNavbar from './MainNavbar.vue';

  export default {
    name: "Layout",
    components: {
      Profile,
      MainNavbar,
    },
    data() {
      return {}
    },
    created() {

    },
    mounted() {

    },
  }
</script>

<style>
  .wrapper {
    display: grid;
    min-height: 100vh;
    grid-template-columns: 280px 1fr;
    background-color: #668663;
  }

  .sidebar {
    padding: 28px 14px;
    color: #fff;
  }

  .main {
    margin: 12px;
    padding: 28px 52px;
    background-color: #fff;
    border-radius: 24px;
  }
</style>