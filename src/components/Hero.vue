<template>
    <div class="hero-container">
        <slider>
            <slider-item v-for="(item, index) in heroList" :key="index" >
              <div>
                <img :src="item.src" class="headline-img"/>
                <div class="overlay">
                  <h1 class="headline-title">{{item.title}}</h1>
                  <p class="headline-desc">{{item.desc}}</p>
                </div>
              </div>
            </slider-item>
        </slider>
    </div>
</template>

<script>
import { Slider, SliderItem } from "vue-easy-slider";

export default {
  name: "hero",
  components: {
    Slider,
    SliderItem
  },
  data() {
    return {
      heroList: [
        {
          src: require("@/assets/images/dota2_headline.jpg"),
          title: "Dota 2",
          desc:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Officia ut eum temporibus voluptatem officiis cumque harum amet incidunt similique? Rem harum alias error sapiente sed nemo quia perspiciatis, nam a."
        },
        {
          src: require("@/assets/images/pubg_headline.jpg"),
          title: "PUBG",
          desc:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Officia ut eum temporibus voluptatem officiis cumque harum amet incidunt similique? Rem harum alias error sapiente sed nemo quia perspiciatis, nam a."
        },
        {
          src: require("@/assets/images/csgo_headline.jpg"),
          title: "CSGO",
          desc:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Officia ut eum temporibus voluptatem officiis cumque harum amet incidunt similique? Rem harum alias error sapiente sed nemo quia perspiciatis, nam a."
        }
      ]
    };
  }
};
</script>

<style scoped>
.hero-container {
  padding-top: 50px;
  height: 450px;
  width: 100%;
  background-color: #292f36;
}
.slider {
  margin: auto;
  height: 400px !important;
  width: 70% !important;
  z-index: 1;
}
.overlay {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.3);
}
.headline-img {
  height: 100%;
  width: 100%;
}
.headline-title {
  max-width: 90%;
  font-family: "Roboto", sans-serif;
  font-weight: bold;
  margin: 230px 0px 5px 60px;
  color: white;
}
.headline-desc {
  max-width: 90%;
  font-family: "Roboto", sans-serif;
  font-size: 16px;
  font-weight: 400;
  margin: 0px 0px 0px 60px;
  color: white;
}
</style>
 