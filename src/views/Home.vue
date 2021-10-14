<template>
  <div class="home">
    <Menu />
    <Feed />
    <MakeLogin />
  </div>
</template>

<script>
import Menu from "@/components/Menu.vue";
import Feed from "@/components/Feed.vue";
import MakeLogin from "@/components/MakeLogin.vue";

export default {
  name: "Home",
  components: {
    Menu,
    Feed,
    MakeLogin,
  },
};
</script>

<style scoped>
.home {
  width: 80vw;
  padding-top: 20px;
  display: flex;
  flex-direction: row;
  align-self: center;
  overflow: hidden;
}
</style>