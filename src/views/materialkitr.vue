<template>
  <div class="fulldiv">
    <div>
      <b-jumbotron class="p-0 top-jumbotron" id="topid">
        <!-- Navigation Bar -->
        <Navbarheader msg="Material Kit Pro">
          <b-nav-item
            href="#"
            slot="navlinks"
            v-for="link in navlinks"
            v-bind:key="link.index"
            v-scroll-to="link.divid"
          >
            <span style="color:#fff" v-if="link.icon1">
              <font-awesome-icon :icon="['fas', 'th']" class="mr-1 small"/>
            </span>
            <span style="color:#fff" v-if="link.icon2">
              <font-awesome-icon :icon="['fas', 'dumbbell']" class="mr-1 small"/>
            </span>
            <span style="color:#fff" v-if="link.icon3">
              <font-awesome-icon :icon="['fas', 'envelope-open-text']" class="mr-1 small"/>
            </span>
            <small v-html="link.name"></small>
            <span style="color:#fff">
              <font-awesome-icon :icon="['fas', 'caret-down']" class="ml-1 small"/>
            </span>
          </b-nav-item>
        </Navbarheader>

        <div class="banner-content">
          <div class="container p-0">
            <div class="addpadding mt-5 pt-5">
              <b-col md="6" sm="9" cols="12" class="p-0">
                <div class="main-banner-content text-white text-left">
                  <div class="mb-3">
                    <h2 class="font-weight-bolder banner-header">Your Story Starts With Us</h2>
                  </div>
                  <div>
                    <div class="banner-text mb-3">
                      Every landing page needs a small description after the big bold title,
                      that's why we added this text here. Add here all the information that can
                      make you or your product create the first impression.
                    </div>
                  </div>
                  <button type="button" class="px-4 py-2 btn btn-danger">
                    <small>
                      <font-awesome-icon :icon="['fas', 'caret-right']" class="mr-2"/>Watch Video
                    </small>
                  </button>
                </div>
              </b-col>
            </div>
          </div>
        </div>
      </b-jumbotron>
    </div>

    <div class="oversection mx-4 px-2 shadow p-3 mb-0 bg-white rounded">
      <b-col md="10" class="mx-auto">
        <div class="pt-4" id="components">
          <b-row>
            <b-col md="8" class="mx-auto">
              <!-- section header -->
              <divheaders>
                <div class="divh3" slot="h3tag">{{ productHeader }}</div>
                <div slot="ptag" class="header-text">{{ productDescription }}</div>
              </divheaders>
            </b-col>
          </b-row>
        </div>
        <!-- component used -->
        <div class="my-4 pt-3">
          <productspecs></productspecs>
        </div>
        <div id="section" class="mt-5 pt-5">
          <b-row>
            <b-col md="10" class="mx-auto">
              <!-- section header -->
              <divheaders>
                <div class="divh3" slot="h3tag">{{ teamHeader }}</div>
              </divheaders>
            </b-col>
          </b-row>
          <div class="mt-2">
            <!-- team members display -->
            <teammedia></teammedia>
          </div>
        </div>

        <div id="example" class="pt-5">
          <b-row>
            <b-col md="8" class="mx-auto">
              <!-- section header -->
              <divheaders>
                <div class="divh3" slot="h3tag">{{ workHeader }}</div>
                <div slot="ptag" class="pt-4 workdesc">{{ workDescription }}</div>
              </divheaders>

              <b-row class="mb-3">
                <b-col md="6">
                  <input
                    type="text"
                    placeholder="Your Name"
                    class="w-100 small border-top-0 border-right-0 border-left-0 border workcolor"
                  >
                </b-col>
                <b-col md="6">
                  <input
                    type="text"
                    placeholder="Your Email"
                    class="w-100 small border-top-0 border-right-0 border-left-0 border workcolor"
                  >
                </b-col>
              </b-row>
              <b-row>
                <b-col md="12">
                  <textarea
                    rows="4"
                    placeholder="Your Message"
                    class="w-100 small border-top-0 border-right-0 border-left-0 border workcolor your-msg-txtarea"
                  ></textarea>
                </b-col>
              </b-row>
              <div class="mt-3 mb-5 text-center">
                <button type="button" class="btn p-2 px-3 sndbtn">Send Message</button>
              </div>
            </b-col>
          </b-row>
        </div>
      </b-col>
    </div>
    <div class="mt-5">
      <sfooter brandnm="MaterialKit"></sfooter>
    </div>
  </div>
</template>

<script>
import Navbarheader from "@/components/Navbarheader.vue";
import divheaders from "@/components/divheaders.vue";
import productspecs from "@/components/productspecs.vue";
import teammedia from "@/components/teammedia.vue";
import sfooter from "@/components/sarasfooter.vue";

export default {
  components: {
    Navbarheader,
    divheaders,
    productspecs,
    teammedia,
    sfooter
  },
  data() {
    return {
      navlinks: [
        {
          name: "Components",
          divid: "#components",
          icon1: true,
          icon2: false,
          icon3: false
        },
        {
          name: "Sections",
          divid: "#section",
          icon1: false,
          icon2: true,
          icon3: false
        },
        {
          name: "Examples",
          divid: "#example",
          icon1: false,
          icon2: false,
          icon3: true
        }
      ],
      productHeader: "Let's talk product",
      productDescription:
        "This is the paragraph where you can write more details about your product. Keep you user engaged by providing meaningful information. Remember that by this time, the user is curious, otherwise he wouldn't scroll to get here. Add a button if you want the user to see more.",
      teamHeader: "Here is our team",
      workHeader: "Work with us",
      workDescription:
        "Divide details about your product or agency work into parts. Write a fewlines about each one bout each one and contact us about any further collaboration. We will respond getback to you in a couple of hours."
    };
  }
};
</script>

<style lang="scss">
@import "../assets/scss/materialkitr/materialkitr.scss";
</style>
