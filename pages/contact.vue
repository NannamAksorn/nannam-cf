<template>
  <div class="container">
    <h1>CONTACT ME</h1>
    <br />
    <div class="contact--grid">
      <!-- email -->
      <span class="contact--item">
        <p class="title">
          <img
            src="https://cdn.iconscout.com/icon/premium/png-256-thumb/email-2262184-1883225.png"
            alt="email"
            width="30"
            height="30"
          />EMAIL:
        </p>
        <p
          v-tooltip="'Click to copy'"
          class="copy"
          @click="copy('nannam.aksorn@gmail.com')"
        >
          nannam.aksorn@gmail.com
        </p>
      </span>
      <!-- Github -->
      <a
        href="https://github.com/NannamAksorn"
        target="_blank"
        class="contact--item"
      >
        <p class="title">
          <img
            src="https://cdn.iconscout.com/icon/free/png-256/github-159-721954.png"
            alt="github"
            width="30"
            height="30"
          />GITHUB:
        </p>
        <p class="link">github.com/NannamAksorn</p>
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  methods: {
    copy(text: string): void {
      navigator.clipboard.writeText(text)
      this.$toast.success(`Copied, ${text}`).goAway(1000)
    },
  },
})
</script>

<style lang="scss">
.copy {
  color: gold;
  font-size: 18px;
  cursor: pointer;
  padding: 0.2rem 1rem;
  transition: all 0.3s;
  border-radius: 0.5rem;
  &:hover {
    background: #0005;
  }
}
.link {
  font-size: 18px;
  cursor: pointer;
  padding: 0.2rem 1rem;
  transition: all 0.3s;
  border-radius: 0.5rem;
  &:hover {
    background: #0005;
  }
}

.contact--grid {
  display: grid;
  grid-column-gap: 1rem;
}

.contact--item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 1rem;
}
.title {
  display: flex;
  align-items: center;
}
</style>
