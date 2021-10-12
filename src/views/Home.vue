<template>
  <div class="home">
    <Menu />
  </div>
</template>

<script>
import Menu from "@/components/Menu.vue";

export default {
  name: "Home",
  components: {
    Menu,
  },
};
</script>

<style scoped>
.home {
  display: flex;
  flex-direction: row;
}
</style>