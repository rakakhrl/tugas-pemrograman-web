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
        <h3 class="section-title">FAQ</h3>
        <div class="categories">
          <vue-faq-accordion 
            :items="faqItems"
            activeColor="#56e39f"
            borderColor="#292f36"
            fontCOlor="#292f36"
            class="faq-accordion"
          />
        </div>
      </div>
    </div>
    <footer-component />
  </div>
</template>

<script>
import {
  Navbar,
  Hero,
  Thumbnail,
  BrowseButton,
  FooterComponent
} from "@/components";
import VueFaqAccordion from "vue-faq-accordion";

export default {
  name: "app",
  components: {
    Navbar,
    Hero,
    Thumbnail,
    BrowseButton,
    VueFaqAccordion,
    FooterComponent
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
          count: "20"
        }
      ],
      faqItems: [
        {
          title: "What is E-News?",
          value:
            "E-News.com is a website where anyone can read and write articles about E-Sports.",
          category: "General Questions"
        },
        {
          title: "Who can write on E-News?",
          value:
            "E-News is an open publishing platform, and we welcome anyone to create an account and share their stories with our community. There is no approval process. When you are ready to publish, it immediately becomes available for reading and sharing.",
          category: "General Questions"
        },
        {
          title: "Write an article",
          value:
            'To begin writing a new article, click the "Create Article" button.',
          category: "Contributing"
        },
        {
          title: "Liked an article",
          value:
            "Click the thumbs up icon under a article. Your likes will help an article to become more popular.",
          category: "Contributing"
        },
        {
          title: "Report an article",
          value:
            "If you feel an article is not following our guidelines, you can report the article by clicking the flag icon and file a report.",
          category: "Contributing"
        }
      ]
    };
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Roboto:400,700");
@import url("https://fonts.googleapis.com/css?family=Lato:400,700");
@import url("https://fonts.googleapis.com/css?family=Righteous");

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

.faq-accordion {
  font-family: "Lato", sans-serif;
}
</style>
