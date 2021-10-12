<template>
  <div class="feed">
    <div class="search-container">
      <div class="search-input-container">
        <div class="search-icon-container">
          <img
            class="search-icon"
            src="../assets/icons/search_icon.svg"
            alt=""
            srcset=""
          />
        </div>
        <input
          type="text"
          name="search-input"
          id="search-input"
          placeholder="Buscar no Twitter"
        />
      </div>
      <img
        class="search-settings"
        src="../assets/icons/settings_icon.svg"
        alt=""
        srcset=""
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "Feed",
};
</script>

<style scoped>
.feed {
  width: 50vw;
  height: 100vh;
  margin: 1px;
  padding-left: 20px;
  padding-right: 20px;
  display: flex;
  flex-direction: column;
  border-left: rgba(255, 255, 255, 0.527);
  border-right: rgba(255, 255, 255, 0.527);;
  border-style: solid;
  border-width: thin;
}

.search-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.search-input-container {
  width: 90%;
  display: flex;
  flex-direction: row;
}

.search-icon-container {
  height: 40px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  border-top-left-radius: 30px;
  border-bottom-left-radius: 30px;
  background-color: rgb(35, 38, 44);
}

.search-icon {
  width: 18px;
  height: 18px;
  padding-left: 20px;
}

#search-input {
  width: 100%;
  height: 40px;
  padding-left: 20px;
  font-size: 15px;
  border-radius: 30px;
  border-top-left-radius: 0px;
  border-bottom-left-radius: 0px;
  color: white;
  background-color: rgb(35, 38, 44);
}

#search-input:focus {
  outline: none;
}

.search-settings {
  cursor: pointer;
}
</style>