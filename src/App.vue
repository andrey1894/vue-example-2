<template>
  <AppHeader />
  <div class="app-wrapper">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view />
  </div>
  <AppFooter />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import AppHeader from '@/components/AppHeader.vue'
import AppFooter from '@/components/AppFooter.vue'

export default defineComponent({
  name: 'App',

  components: {
    AppHeader,
    AppFooter,
  },
})
</script>

<style lang="scss">
@import '@/styles';

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  text-align: center;
  color: #2c3e50;

  .app-wrapper {
    flex: 1;
  }
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: var(--bs-success);
    }
  }
}
</style>
