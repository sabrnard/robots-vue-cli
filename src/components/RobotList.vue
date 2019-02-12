<template>
  <section class="robots" id="robots">
    <RobotItem
      v-for="r in robots"
      :key="r.id"
      :robot="r"
    />
  </section>
</template>

<script>
// on utilise movie dans list donc on importe RobotItem.vue
import RobotItem from "./RobotItem.vue";

export default {
  props: ["robots"],
  components: {
    RobotItem
  }
};
</script>

<style>
</style>
