<template>
  <div class="menu">
    <img
      class="logo"
      src="../assets/icons/twitter_white.svg"
      alt=""
      srcset=""
    />

    <div class="buttons-container">
      <a href="/">
        <button>
          <img
            class="button-icon"
            src="../assets/icons/explore_icon.svg"
            alt=""
          />
          <span>Explorar</span>
        </button></a
      >
      <a href="/settings">
        <button>
          <img
            class="button-icon"
            src="../assets/icons/settings_icon.svg"
            alt=""
          />
          <span>Configurações</span>
        </button></a
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "Menu",
};
</script>

<style scoped>
.menu {
  width: 25vw;
  padding-left: 50px;
  display: flex;
  flex-direction: column;
}

.logo {
  width: 28px;
  height: 28px;
  margin-top: 20px;
  margin-left: 10px;
}

.buttons-container {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
}

button {
  width: 200px;
  height: 50px;
  margin-bottom: 15px;
  padding: 10px;
  display: flex;
  flex-direction: row;
  align-items: center;
  color: white;
  text-align: start;
  border-radius: 30px;
  background-color: transparent;
  cursor: pointer;
}

button:hover {
  background-color: rgba(255, 255, 255, 0.096);
}

button span {
  font-family: "Open Sans", sans-serif;
  font-size: 18px;
  font-weight: 700;
}

.button-icon {
  padding-right: 10px;
}
</style>