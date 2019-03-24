<template>
  <div class="ui secondary pointing menu">
    <a href="/" class="active item">
      Image storage
    </a>

    <div class="right menu">
      <div v-if="isLoggedIn" class="horizontal">
        <a class="item">Galleries</a>
        <a class="item">Upload</a>
        <a class="item">Logout</a>
      </div>

      <a v-else href="#" class="ui item" @click="login">
        Login
      </a>
    </div>
  </div>
</template>

<script>
  import { mapActions, mapGetters } from 'vuex';

  export default {
    name: 'AppHeader',
    computed: mapGetters(['isLoggedIn']),
    methods: mapActions(['login'])
  }
</script>

<style>
  .horizontal {
    display: flex;
    flex-direction: row;
  }
</style>
