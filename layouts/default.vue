<template>
  <div class="layout">
    <nav class="navbar">
      <div v-for="item in navItems" :key="item.title" class="navbar--item">
        <NuxtLink :to="item.link">
          {{ item.title }}
        </NuxtLink>
      </div>
    </nav>
    <Nuxt />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      navItems: [
        { title: 'ABOUT', link: '/' },
        { title: 'WORK', link: '/work' },
        { title: 'CONTACT', link: '/contact' },
      ],
    }
  },
})
</script>
<style lang="scss">
html {
  background: #0f111a;
  color: #aaa;
  font-family: 'Montserrat', 'Source Sans Pro', -apple-system,
    BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  overflow: hidden;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
.layout {
  display: flex;
  @media screen and (max-width: 650px) {
    flex-direction: column;
  }
}
.navbar {
  padding: 2px 1em;
  background: #090b10;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  box-shadow: 6px 6px 12px #040507, -6px -6px 12px #0e1119;

  @media screen and (max-width: 650px) {
    height: 30px;
    justify-content: space-around;
    flex-direction: row;
  }
}
.navbar--item {
  padding: 0.8em 0;
  margin: 0.3em 0;
  cursor: pointer;
}
.navbar--item:hover {
  color: #fff;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
