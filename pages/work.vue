<template>
  <div class="container">
    <h1>My Work</h1>
    <br />
    <div class="work--item-group">
      <!-- TU AROUND -->
      <div class="work--item">
        <img src="/project/tuaround/main.png" width="300" />
        <p class="caption">TUAROUND - Vehicle tracking</p>
      </div>
      <!-- CONNECTIVE LEARNING -->
      <div class="work--item">
        <img src="/project/connectiveLearning/main.png" width="300" />
        <p class="caption">CONNECTIVE LEARNING - Video Search and Summarize</p>
      </div>
      <!-- BIG EYE -->
      <div class="work--item">
        <img src="/project/bigEye/main.png" width="300" />
        <p class="caption">BIG EYE - Facial Recognition + Chatbot</p>
      </div>
      <!-- HELMET HUNTER -->
      <div class="work--item">
        <img src="/project/helmetHunter/main.png" width="300" />
        <p class="caption">Helmet Hunter - Motorcycle Helmet Detection</p>
      </div>
      <!-- SUDOKU SOLVER -->
      <div class="work--item">
        <img src="/project/sudokuSolver/main.png" width="300" />
        <p class="caption">SUDOKU SOLVER & GENERATOR</p>
      </div>
      <!-- SMART PLUG -->
      <div class="work--item">
        <img src="/project/smartPlug/main.png" width="300" />
        <p class="caption">SMART PLUG - IoT Socket</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.work--item-group {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  height: 95vh;
  overflow: auto;
}
.work--item {
  width: 320px;
  cursor: pointer;
  margin: 1.2em;
  img {
    border-radius: 1rem;
    transition: transform 0.15s;
    &:hover {
      transform: scale(1.1);
    }
  }
  .caption {
    margin-top: 1rem;
  }
}
</style>
