<template>
    <div>
      <h1>Rocks Paper Scissors Lizard Spock Game</h1>
      <RulesModalComponent />
    </div>
  </template>
  <script lang="ts">
  import { defineComponent } from "vue";
  import RulesModalComponent from "./RulesModalComponent.vue";
  export default defineComponent({
    name: "AdvancedGameComponent",
    prop: {},
    components: {
      RulesModalComponent,
    },
  });
  </script>
  <style scoped lang="scss"></style>
  