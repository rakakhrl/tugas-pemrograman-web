<template>
  <div id="app">
    <navbar />
    <div>
      <hero />
      <div class="top-section">
        <h3 class="section-title">TOP CATEGORIES</h3>
        <div class="categories" > 
          <!-- looping for thumbnail component -->
          <div v-for="(item, index) in categoriesList" :key="index">
            <thumbnail :imgSrc="item.src" :title="item.title" :count="item.count"/>
          </div>
          <browse-button/>
        </div>
      </div>
      <div class="bottom-section">
        <h3 class="section-title">FEATURED ARTICLE</h3>
        <!-- accordion component -->
      </div>
    </div>
    <div class="footer">
      <!-- change to footer component soon -->
    </div>
  </div>
</template>

<script>
import { Navbar, Hero, Thumbnail, BrowseButton } from "@/components";

export default {
  name: "app",
  components: {
    Navbar,
    Hero,
    Thumbnail,
    BrowseButton
  },
  data() {
    return {
      categoriesList: [
        {
          src: require("@/assets/images/dota_2.jpg"),
          title: "Dota 2",
          count: "125"
        },
        {
          src: require("@/assets/images/fortnite.jpg"),
          title: "Fortnite",
          count: "81"
        },
        {
          src: require("@/assets/images/lol.jpg"),
          title: "League of Legends",
          count: "60"
        },
        {
          src: require("@/assets/images/pubg.jpg"),
          title: "PUBG",
          count: "54"
        },
        {
          src: require("@/assets/images/warframe.jpg"),
          title: "Warframe",
          count: "47"
        },
        {
          src: require("@/assets/images/fallout76.jpg"),
          title: "Fallout 76",
          count: "27"
        },
        {
          src: require("@/assets/images/csgo.jpg"),
          title: "CSGO",
          count: "23"
        },
        {
          src: require("@/assets/images/hearthstone.jpg"),
          title: "Hearthstone",
          count: "23"
        },
        {
          src: require("@/assets/images/overwatch.jpg"),
          title: "Overwatch",
          count: "120"
        }
      ]
    };
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Roboto:400,700");
@import url("https://fonts.googleapis.com/css?family=Lato:400,700");

::-webkit-scrollbar {
  width: 10px;
  background: transparent;
}

::-webkit-scrollbar-thumb {
  background: #56e39f;
}

.top-section {
  width: 100%;
  border-bottom: 0.75px solid lightgray;
}

.bottom-section {
  width: 100%;
}

.categories {
  height: 500px;
  width: 70%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  padding: 8px 18px;
  box-sizing: border-box;
  margin: 0px auto 30px auto;
}

.section-title {
  text-align: center;
  font-family: "Roboto", sans-serif;
  font-weight: bold;
  color: #292f36;
}

.footer {
  height: 250px;
  width: 100%;
  background-color: #292f36;
  border-top: 4px solid #56e39f;
}
</style>
