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
    <div class="tab-bar-container">
      <button
        class="tab active"
        id="tab-for-you"
        v-on:click="activeTabBarAndText('tab-for-you', 'text-for-you')"
      >
        <span class="tab-text text-active" id="text-for-you">Para você</span>
      </button>
      <button
        class="tab"
        id="tab-covid"
        v-on:click="activeTabBarAndText('tab-covid', 'text-covid')"
      >
        <span class="tab-text" id="text-covid">Covid-19</span>
      </button>
      <button
        class="tab"
        id="tab-trendings"
        v-on:click="activeTabBarAndText('tab-trendings', 'text-trendings')"
      >
        <span class="tab-text" id="text-trendings">Assuntos do Momento</span>
      </button>
      <button
        class="tab"
        id="tab-news"
        v-on:click="activeTabBarAndText('tab-news', 'text-news')"
      >
        <span class="tab-text" id="text-news">Notícias</span>
      </button>
      <button
        class="tab"
        id="tab-sports"
        v-on:click="activeTabBarAndText('tab-sports', 'text-sports')"
      >
        <span class="tab-text" id="text-sports">Esportes</span>
      </button>
    </div>
  </div>
</template>

<script>
var currentTabActived = "tab-for-you";
var currentTabTextActive = "text-for-you";

export default {
  name: "Feed",
  methods: {
    activeTabBarAndText: function (tabId, textId) {
      this.removeCurrentActive(currentTabActived, currentTabTextActive);

      document.getElementById(tabId).className = "tab active";
      document.getElementById(textId).className = "tab-text text-active";

      currentTabActived = tabId;
      currentTabTextActive = textId;
    },
    removeCurrentActive: function (tabId, textId) {
      document.getElementById(tabId).className = "tab";
      document.getElementById(textId).className = "tab-text";
    },
  },
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
  border-right: rgba(255, 255, 255, 0.527);
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

.tab-bar-container {
  width: 100%;
  margin-top: 20px;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}

.tab {
  height: 40px;
  background-color: transparent;
  cursor: pointer;
  color: white;
}

.tab:hover {
  background-color: rgba(255, 255, 255, 0.096);
}

.tab-text {
  padding: 10px;
  font-size: 15px;
  color: gray;
  font-weight: 700;
}

.text-active {
  color: white;
}

.active {
  border-bottom: rgb(29, 155, 240);
  border-style: solid;
}
</style>