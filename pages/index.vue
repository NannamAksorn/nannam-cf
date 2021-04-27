<template>
  <div class="container">
    <div>name: '<span class="about--name">Nannam Aksorn</span>'</div>
    <br />
    <!-- Skill -->
    <section class="section section-skill">
      <div>
        skill: [
        <span v-for="s in skill" :key="s.t"
          >'<span class="about--name">{{ s.t }}</span
          >',</span
        >
        ]
      </div>
    </section>
    <!-- Programming language -->
    <section class="section section-pl">
      <p>{{ programmingLanguage.t }}:</p>
      <div class="pl--icon-group">
        <div
          v-for="pl in programmingLanguage.list"
          :key="pl.t"
          v-tooltip="pl.d"
          class="pl--icon"
        >
          <div>
            <img :src="pl.i" :alt="pl.t" width="100%" height="100%" />
          </div>
          <p>{{ pl.t }}</p>
        </div>
      </div>
    </section>
    <!-- More -->
    <section class="section section-more">
      <ul class="techspec-list" role="list">
        <li class="grid-item">
          <strong class="title">Typing Speed:</strong
          ><span class="spec--detail"> ~100 WPM</span>
        </li>
        <li class="grid-item">
          <strong class="title">TOEIC:</strong
          ><span class="spec--detail">910</span>
        </li>
        <li class="grid-item">
          <strong class="title">Education:</strong
          ><span class="spec--detail"
            >Bachelor - Computer Enginnering @SIIT [GPA 3.3]</span
          >
        </li>
      </ul>
    </section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      name: 'Nannam Aksorn',
      skill: [
        { t: 'Frontend' },
        { t: 'Backend' },
        { t: 'Devops' },
        { t: 'Databases' },
      ],
      programmingLanguage: {
        t: 'Programming Languages',
        list: [
          {
            t: 'Python',
            i:
              'https://cdn.iconscout.com/icon/free/png-256/python-3628999-3030224.png',
            d:
              "I used Python alot for researching, Machine Learning, quick small project. People usually say it slow, but I've never notice the different.",
          },
          {
            t: 'JavaScript',
            i:
              'https://cdn.iconscout.com/icon/free/png-512/javascript-1-225993.png',
            d:
              'Very comfortable using JS for webapp and backend. I would go with TypeScript for large project.',
          },
          {
            t: 'TypeScript',
            i:
              'https://cdn.iconscout.com/icon/free/png-512/typescript-1174965.png',
            d:
              'My main language right now. It foreced me to write a better, bug free code.',
          },
          {
            t: 'Golang',
            i: '/icon/golang.svg',
            d:
              'I love the performance and simplicity of the language. I have used it for many microservices, never got any problem.',
          },
          {
            t: 'Java',
            i:
              'https://cdn.iconscout.com/icon/free/png-256/java-3628857-3029997.png',
            d:
              "First Language I learned. It's alright, if the project is well-structured. I just felt old when using Java.",
          },
          {
            t: 'PHP',
            i:
              'https://cdn.iconscout.com/icon/free/png-256/php-3629567-3032350.png',
            d:
              'Hated it! Reading PHP just make me sad. I When I got a project to fix PHP code or write customize WordPress, I would end up rewrite everything with my preferred languages.',
          },
          {
            t: 'C family',
            i:
              'https://cdn.iconscout.com/icon/free/png-256/c-programming-569564.png',
            d:
              "I can write C, slowly, but I'll get it to work eventually. I'll use it, if I really need to.",
          },
        ],
      },
    }
  },
})
</script>

<style lang="scss">
.about--name {
  color: #ffcb6b;
  font-size: 1.2rem;
  font-weight: bold;
  cursor: pointer;
  padding: 0.4rem;
  border-radius: 0.5rem;
  animation: name_appear 2s;
  transition: all 0.3s;
  &:hover {
    background: black;
  }
}

.section {
  padding: 1.3em 0;
  border-top: 1px solid #d2d2d722;
  width: 85%;
  max-width: 1000px;
}

.section-skill {
  overflow: auto;
}

.pl--icon-group {
  margin-top: 1.2rem;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
.pl--icon {
  flex: 1 0 13%;
  display: flex;

  justify-content: center;
  align-items: center;
  flex-direction: column;
  font-size: 11px;
  img {
    padding: 0.4rem;
    border-radius: 0.4rem;
    width: 45px;
    height: 45px;
    transition: all 0.3s;
    cursor: pointer;
    &:hover {
      background: #8883;
    }
  }
  p {
    cursor: pointer;
  }
}

.techspec-list {
  font-size: 14px;
}
.spec--detail {
  padding-left: 1rem;
}

@keyframes name_appear {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
