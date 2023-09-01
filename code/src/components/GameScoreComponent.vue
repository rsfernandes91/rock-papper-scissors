<template>
  <div class="container">
    <div class="score">
      <div class="game-title">
        <h3>ROCK</h3>
        <h3>PAPER</h3>
        <h3>SCISSORS</h3>
      </div>
      <div class="score-container">
        <div>
          <h5>Score</h5>
          <h2 class="score-number">{{ score }}</h2>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  score: number;
}>();
</script>
<style scoped lang="scss">
.container {
  display: flex;
  justify-content: center;
  align-items: flex-start;
}

.score {
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  margin-top: 20px;
  width: 50%;
  border-radius: 10px;
  border: 1px solid white;
  color: #000;
  justify-content: space-between;
}

.game-title h3 {
  margin-left: 15px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin: 0;
  color: white;
}

.score-container {
  align-items: center;
  display: flex;
  justify-content: center;
  background-color: white;
  border-radius: 5px;
  width: 80px;
  height: 60px;
}
</style>
