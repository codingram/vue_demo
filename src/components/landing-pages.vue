
<template>
  <div>
    <!-- created by roshan -->
    
      <div class="landing-main">
      <b-row class="m-auto">
        <b-col md=4 v-for="card in cards" v-bind:key="card.index">
          <div class="landing-content rounded-0">
            <b-card :img-src="card.cardimg" img-alt="Image" img-top tag="article" class="mb-2 border-0 text-left rounded-0">
              <div class="landing-titlee" :class="card.textcolor">{{card.heading}} <span :class="card.spannclass">{{card.spantext}}</span> </div>
              <b-card-text>
                <div class="landing-textt" :class="card.textcolor">{{card.para}}</div>
              </b-card-text>
  
            </b-card>
          </div>
        </b-col>
      </b-row>
      </div>
   
  
  </div>
</template>

<script>
import images1 from "../assets/web2.jpg";
import images2 from "../assets/web3.jpg";
import images3 from "../assets/web4.jpg";
import images4 from "../assets/web5.png";
import images5 from "../assets/web6.jpg";
import images6 from "../assets/web7.png";
import images7 from "../assets/web9.jpeg";
export default {
  data() {
    return {
      cards: [
        {
          cardimg: images1,
          heading: "Product landing ",
          para: "You can use this page to promote your product or a store."
        },
        {
          cardimg: images2,
          heading: "Real estate landin",
          spantext: "New!",
          spannclass: "bg-danger  text-white pb-1 px-1 fontless",
          para: "You can use this page to promote your real estate."
        },
        {
          cardimg: images3,
          heading: "Restaurant landing",
          para: "You can use this page to promote your restaurant."
        },
        {
          cardimg: images4,
          heading: "App landing",
          para: "You can use this page to promote your restaurant."
        },
        {
          cardimg: images5,
          heading: "Company landing",
          para: "You can use this page to promote your restaurant."
        },
        {
          cardimg: images6,
          heading: "Fullpage scrolling",
          spantext: "New!",
          spannclass: "bg-danger  text-white pb-1 px-1 fontless",
          para: "You can use this page to promote your restaurant."
        },
        {
          cardimg: images2,
          heading: "Service landing",
          para: "You can use this page to promote your restaurant."
        },
        {
          cardimg: images7,
          heading: "Coming soon",
          para:
            "Feel free to contact us with your ideas about new pages and components.",
            textcolor:"changecolor"
        }
      ]
    };
  }
};
</script>

<style lang="scss">
@import "../assets/scss/incline-website/landing-pages.scss";
</style>
