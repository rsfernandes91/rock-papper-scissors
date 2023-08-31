<template>
  <div>
    <h1>Teste Novo Component</h1>
    <RulesModalComponent />
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import RulesModalComponent from "./RulesModalComponent.vue";
export default defineComponent({
  name: "GameChallenge",
  prop: {},
  components: {
    RulesModalComponent,
  },
});
</script>
<style scoped lang="scss"></style>
