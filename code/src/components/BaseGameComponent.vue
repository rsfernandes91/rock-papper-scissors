<template>
  <div class="base">
    <GameScoreComponent :score="10" />
    <button @click="rockPaperScissorsStart('rock')">Rock</button>
    <button @click="rockPaperScissorsStart('paper')">Paper</button>
    <button @click="rockPaperScissorsStart('scissors')">SCISSORS</button>

    <h2>{{ whoWonTheGame }}</h2>
    <RulesModalComponent />
  </div>
</template>
<script setup lang="ts">
import RulesModalComponent from "./RulesModalComponent.vue";
import GameScoreComponent from "./GameScoreComponent.vue";
import { ref } from "vue";
const whoWonTheGame = ref<string>();
function randomChoice() {
  let computerOptions = ["rock", "paper", "scissors"];
  let randomIndex = Math.floor(Math.random() * 3);
  return computerOptions[randomIndex];
}

function rockPaperScissorsStart(playerChoice: string) {
  let computerChoice = randomChoice();
  whoWonTheGame.value = getWinner(playerChoice, computerChoice);
}

function getWinner(playerChoice: string, computerChoice: string) {
  switch (playerChoice) {
    case "rock":
      switch (computerChoice) {
        case "rock":
          return "DRAW!";
        case "paper":
          return "YOU LOST!";
        case "scissors":
          return "YOU WIN!";
      }
      break;
    case "paper":
      switch (computerChoice) {
        case "rock":
          return "YOU WIN!";
        case "paper":
          return "DRAW!";
        case "scissors":
          return "YOU LOST!";
      }
      break;
    case "scissors":
      switch (computerChoice) {
        case "rock":
          return "YOU LOST!";
        case "paper":
          return "YOU WIN!";
        case "scissors":
          return "DRAW!";
      }
      break;
    default:
      return "Wrong Choice!";
  }
}
</script>
<style scoped lang="scss">
.base {
  @media (min-width: 1366px) {
    background: radial-gradient(circle, hsl(214, 47%, 23%), hsl(237, 49%, 15%));
    width: 80%;
    height: 60%;
  }

  @media (max-width: 375px) {
  }
}
</style>
