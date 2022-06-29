<template>
  <nav-bar />
  <hero-main />
  <ServicesContent class="services-content" />
  <ServicesBottom class="services-bottom" />
  <FooterMain />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import NavBar from 'components/NavBar.vue'
import HeroMain from 'components/HeroMain.vue'
import ServicesContent from 'components/ServicesContent.vue'
import ServicesBottom from 'components/ServicesBottom.vue'
import FooterMain from 'components/FooterMain.vue'

export default defineComponent({
  name: 'App',
  components: {
    NavBar,
    HeroMain,
    ServicesContent,
    ServicesBottom,
    FooterMain,
  },
})
</script>

<style lang="scss">
* {
  margin: 0px;
  padding: 0px;

  box-sizing: border-box;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-family: '微软雅黑', 'Source Han Sans', sans-serif;
  // font-size: 16px;

  ul {
    padding: 0;
    margin: 0;
  }
  li {
    list-style: none;
  }
  a {
    text-decoration: none;
  }
  select,
  input,
  label,
  button {
    vertical-align: middle;
  }
}

#app {
  .services-content {
    margin: 0 auto;
    margin-top: -9rem;
  }
  .services-bottom {
    margin-top: 100px;
    margin-bottom: 100px;
  }
}
</style>
