<template>
  <div class="base">
    <GameScoreComponent :score="10" />
    <RulesModalComponent />
  </div>
</template>
<script setup lang="ts">
import RulesModalComponent from "./RulesModalComponent.vue";
import GameScoreComponent from "./GameScoreComponent.vue";
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
