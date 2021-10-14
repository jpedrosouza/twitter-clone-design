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
    <div class="feed-cards-container">
      <div class="highlight-card">
        <img
          class="highlight-image"
          src="https://www.maxmilhas.com.br/blog/wp-content/uploads/2019/05/Mineir%C3%A3o-Est%C3%A1dios-da-Copa-Am%C3%A9rica-2019.jpg"
          alt=""
        />
        <div class="highlight-text-container">
          <span class="highlight-subtitle"
            >Campeonato Brasileiro . AO VIVO</span
          >
          <span class="highlight-title">Atlético 3 X 1 Santos</span>
          <span class="highlight-subtitle">Assuntos do Momento: Hulk</span>
        </div>
      </div>
      <div class="news-cards-container">
        <div class="news-card">
          <div class="news-card-text-container">
            <span class="news-card-title">Atlético</span>
            <span class="news-card-subject"
              >Mais 3 pontos no Campeonato Brasileiro</span
            >
          </div>
          <img
            class="news-card-image"
            src="https://media-exp1.licdn.com/dms/image/C4E0BAQEjCSXYvZGMtw/company-logo_200_200/0/1606332694110?e=2159024400&v=beta&t=EqEHb6y82_wPRPW85Ivcufv_4CBnRUB44YAzqg6P4tQ"
            alt=""
          />
        </div>
        <div class="news-card">
          <div class="news-card-text-container">
            <span class="news-card-title">Flamengo</span>
            <span class="news-card-subject"
              >Mais 3 pontos no Campeonato Brasileiro</span
            >
          </div>
          <img
            class="news-card-image"
            src="https://i.pinimg.com/originals/4f/0a/b6/4f0ab6e9d01b3936bfdeaea88947cacc.png"
            alt=""
          />
        </div>
        <div class="news-card">
          <div class="news-card-text-container">
            <span class="news-card-title">Atlético</span>
            <span class="news-card-subject"
              >Mais 3 pontos no Campeonato Brasileiro</span
            >
          </div>
          <img
            class="news-card-image"
            src="https://media-exp1.licdn.com/dms/image/C4E0BAQEjCSXYvZGMtw/company-logo_200_200/0/1606332694110?e=2159024400&v=beta&t=EqEHb6y82_wPRPW85Ivcufv_4CBnRUB44YAzqg6P4tQ"
            alt=""
          />
        </div>
        <div class="news-card">
          <div class="news-card-text-container">
            <span class="news-card-title">Flamengo</span>
            <span class="news-card-subject"
              >Mais 3 pontos no Campeonato Brasileiro</span
            >
          </div>
          <img
            class="news-card-image"
            src="https://i.pinimg.com/originals/4f/0a/b6/4f0ab6e9d01b3936bfdeaea88947cacc.png"
            alt=""
          />
        </div>
      </div>
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

.feed-cards-container {
  width: 100%;
  height: 100%;
  margin-top: 10px;
  display: flex;
  flex-direction: column;
  overflow-y: auto;
}

.feed-cards-container::-webkit-scrollbar {
  display: none;
}

.highlight-card {
  width: 100%;
  height: 450px;
  cursor: pointer;
}

.highlight-image {
  width: 100%;
  filter: brightness(30%);
}

.highlight-text-container {
  position: relative;
  left: 20px;
  bottom: 100px;
  display: flex;
  flex-direction: column;
}

.highlight-title {
  padding-top: 5px;
  padding-bottom: 5px;
  color: white;
  font-weight: 700;
  font-size: 20px;
}

.highlight-subtitle {
  color: white;
  font-weight: 500;
  font-size: 14px;
}

.news-cards-container {
  margin-top: 5px;
  margin-bottom: 100px;
  display: flex;
  flex-direction: column;
}

.news-card {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  cursor: pointer;
  border-radius: 10px;
}

.news-card:hover {
  background-color: rgba(255, 255, 255, 0.096);
}

.news-card-text-container {
  margin-top: 20px;
  padding: 10px;
  display: flex;
  flex-direction: column;
  color: white;
}

.news-card-title {
  font-weight: 700;
  margin-bottom: 10px;
}

.news-card-image {
  width: 80px;
  height: 80px;
  padding: 10px;
  border-radius: 20px;
}
</style>