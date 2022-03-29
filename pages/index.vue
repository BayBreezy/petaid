<template>
  <div class="pattern">
    <Nav />
    <v-container fluid style="height: 100vh" class="pa-0 fill-height">
      <v-row no-gutters align="center">
        <v-spacer />
        <v-col md="4" cols="11">
          <h1 id="title" class="text-md-h2 text-h2 font-weight-medium">
            Let us take care of your pet for you
          </h1>
          <p id="statement" class="text-h5 mb-7 mt-10">
            We understand that they mean a lot. That is why we provide excellent
            service.
          </p>
          <div class="cta">
            <v-btn
              color="primary"
              min-width="150"
              rounded
              min-height="50"
              class="font-weight-light"
              >See Services</v-btn
            >
            <v-btn
              color="primary"
              min-width="150"
              rounded
              outlined
              min-height="50"
              class="font-weight-light ml-3"
              >Get Quote</v-btn
            >
          </div>
        </v-col>
        <v-spacer />
        <v-col v-if="$vuetify.breakpoint.mdAndUp" md="6">
          <v-img
            id="himage"
            height="100vh"
            class="rounded-lg"
            src="/home-pup.jpg"
          >
            <template #placeholder>
              <v-row align="center" justify="center" class="fill-height">
                <v-progress-circular
                  width="2"
                  size="150"
                  color="primary"
                  indeterminate
                ></v-progress-circular>
              </v-row>
            </template>
          </v-img>
        </v-col>
      </v-row>
    </v-container>
    <br /><br />
    <v-container class="mt-md-15">
      <h2 id="reviews" class="primary--text text-md-h4">
        Why our customers love us
      </h2>
      <br /><br />
      <v-slide-group
        class="mt-md-10"
        show-arrows="desktop"
        next-icon="mdi-menu-right"
        prev-icon="mdi-menu-left"
        center-active
      >
        <v-slide-item v-for="n in 15" :key="`customerReview${n}`" class="pa-2">
          <v-card class="mr-3 ma-2 rev el" width="300">
            <v-card-title>Simply Awesome</v-card-title>
            <v-card-subtitle>
              <v-rating
                :value="5"
                background-color="grey lighten-2"
                dense
                small
                color="yellow darken-2"
              ></v-rating>
            </v-card-subtitle>
            <v-card-text>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias
              totam sed quam dolorem quae et.
            </v-card-text>
            <v-card-actions> - Sasha G. </v-card-actions>
          </v-card>
        </v-slide-item>
      </v-slide-group>
    </v-container>
    <v-container class="mt-md-15">
      <h2 id="products" class="primary--text text-md-h4">
        Products to keep them happy
      </h2>
      <br /><br />
      <v-slide-group
        next-icon="mdi-menu-right"
        show-arrows="desktop"
        prev-icon="mdi-menu-left"
        center-active
      >
        <v-slide-item v-for="n in 15" :key="`customerReview${n}`" class="mr-5">
          <v-card hover height="350" class="el ma-2 prod" width="300">
            <v-img
              class=""
              height="100%"
              src="https://images.pexels.com/photos/7310213/pexels-photo-7310213.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
            >
              <v-row
                no-gutters
                align="end"
                justify="center"
                class="fill-height"
              >
                <v-col class="pa-3 white" cols="12">
                  <h3 class="text-md-6">Puppy Chow</h3>
                  <p
                    class="mb-0 success--text text-md-subtitle-1 font-weight-medium"
                  >
                    $50.00
                  </p>
                </v-col>
              </v-row>
            </v-img>
          </v-card>
        </v-slide-item>
      </v-slide-group>
    </v-container>
    <v-container class="mt-md-15">
      <h2 id="gallery" class="primary--text text-md-h4">Gallery</h2>
      <br />
      <v-slide-group
        next-icon="mdi-menu-right"
        prev-icon="mdi-menu-left"
        show-arrows="desktop"
        center-active
      >
        <v-slide-item
          v-for="(d, i) in dogs"
          :key="`gallerImage${i}`"
          class="mr-5"
        >
          <v-card hover height="350" class="el ma-2 gallery" width="300">
            <v-img class="" height="100%" :src="d">
              <template #placeholder>
                <v-row class="fill-height align-center justify-center">
                  <v-progress-circular
                    indeterminate
                    width="2"
                    color="primary"
                    size="150"
                  ></v-progress-circular>
                </v-row>
              </template>
            </v-img>
          </v-card>
        </v-slide-item>
      </v-slide-group>
    </v-container>
    <br />
    <v-img
      width="100vw"
      height="80vh"
      src="https://images.pexels.com/photos/1120049/pexels-photo-1120049.jpeg"
    >
      <v-container id="about-us" class="fill-height">
        <v-row align="center">
          <v-spacer />
          <v-col class="text-center" cols="12" md="5">
            <h1 class="text-md-h2 white--text">About Us</h1>
            <p class="white--text text-md-h6 mt-md-7">
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nesciunt
              consectetur esse perspiciatis nisi error suscipit necessitatibus
              reiciendis porro ipsa est, itaque praesentium ducimus voluptate
              distinctio doloribus rerum. Nemo, quia perferendis.
            </p>
            <v-btn rounded depressed color="white" min-height="50" class="mt-4"
              >Learn More</v-btn
            >
          </v-col>
        </v-row>
      </v-container>
    </v-img>
    <v-container class="mt-md-15">
      <v-row>
        <v-col cols="12" md="6">
          <h1 id="contact-us" class="primary--text text-md-h4">
            Get In Touch Today
          </h1>
          <br /><br />
          <v-form>
            <v-row dense>
              <v-col cols="12">
                <v-text-field outlined label="Name"></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field
                  outlined
                  label="Email"
                  type="email"
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-textarea outlined label="Message"></v-textarea>
              </v-col>
              <v-col cols="12">
                <v-btn min-width="200" rounded min-height="50" color="primary"
                  >Submit</v-btn
                >
              </v-col>
            </v-row>
          </v-form>
        </v-col>
        <v-col md="6">
          <v-img
            height="500"
            class="rounded-lg"
            src="https://images.pexels.com/photos/1661179/pexels-photo-1661179.jpeg"
          ></v-img>
        </v-col>
      </v-row>
    </v-container>
    <br /><br />
    <v-footer padless>
      <v-container>
        <v-row>
          <v-col class="text-center pt-10" cols="12" md="3">
            <v-avatar>
              <nuxt-link to="/">
                <v-img src="/logo.svg"></v-img>
              </nuxt-link>
            </v-avatar>
            <nuxt-link class="text-decoration-none black--text" to="/">
              <span class="font-weight-bold text-md-h5 text-h5 ml-2"
                >Pet<span class="primary--text">Aid</span>
              </span>
            </nuxt-link>
          </v-col>
          <v-spacer />
          <v-col cols="12" md="4" class="pt-10 pr-md-10">
            <h2>Newsletter</h2>
            <p>Stay in up to date with the latest animal news & trends!</p>
            <v-text-field outlined label="Email"></v-text-field>
            <v-btn block min-height="45" color="primary">Subscribe</v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
  </div>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    try {
      let { data } = await $axios.get(
        "https://dog.ceo/api/breeds/image/random/15"
      );
      let dogs = data.message;
      return { dogs };
    } catch (error) {
      console.log(error);
    }
  },
  mounted() {
    let tl = this.$gsap.timeline();
    this.$gsap.from("#himage", {
      opacity: 0,
      duration: 1.7,
    });
    this.$gsap.from(".rev", {
      translateY: -50,
      scrollTrigger: {
        trigger: ".rev",
        toggleActions: "play reset play reset",
      },
      opacity: 0,
      stagger: 0.1,
    });
    this.$gsap.from(".gallery", {
      translateY: -50,
      scrollTrigger: {
        trigger: ".gallery",
        toggleActions: "play reset play reset",
      },
      opacity: 0,
      stagger: 0.1,
    });
    this.$gsap.from(".prod", {
      translateY: -50,
      scrollTrigger: {
        trigger: ".prod",
        toggleActions: "play reset play reset",
      },
      opacity: 0,
      stagger: 0.1,
    });
    tl.from("#title", {
      translateY: -70,
      opacity: 0,
    })
      .from("#statement", {
        translateY: 70,
        opacity: 0,
      })
      .from(".cta", {
        translateY: 70,
        opacity: 0,
      });
  },
};
</script>

<style></style>
