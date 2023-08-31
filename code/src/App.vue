<template>
  <BaseGameComponent />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import BaseGameComponent from "./components/BaseGameComponent.vue";

export default defineComponent({
  name: "App",
  components: {
    BaseGameComponent,
  },
});
</script>

<style lang="scss">
#app {
  font-family: "Barlow Semi Condensed", sans-serif;
  text-align: center;
  margin-top: 60px;
}
</style>
