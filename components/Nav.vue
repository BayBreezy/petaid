<template>
  <div>
    <v-app-bar flat color="rgba(255,255,255,0.9)" fixed height="70">
      <v-container class="fill-height align-center">
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

        <v-spacer />
        <div v-if="$vuetify.breakpoint.mdAndUp">
          <nuxt-link
            v-for="(n, i) in nav"
            :key="`navItem${i}`"
            class="nuxt-link mx-2"
            active-class="font-weight-bold"
            :to="n.link"
            >{{ n.text }}</nuxt-link
          >
        </div>
        <v-spacer v-if="$vuetify.breakpoint.mdAndUp" />
        <v-btn
          v-if="$vuetify.breakpoint.mdAndUp"
          depressed
          color="primary"
          rounded
          class="font-weight-light text-capitalize"
          >Our Services</v-btn
        >
        <div v-else>
          <v-app-bar-nav-icon @click="drawer = !drawer"> </v-app-bar-nav-icon>
        </div>
      </v-container>
    </v-app-bar>
    <v-navigation-drawer app temporary v-model="drawer">
      <v-list nav>
        <template v-for="(n, i) in nav">
          <v-list-item :key="`navMobile${i}`" nuxt :to="n.link">
            <v-list-item-title>
              {{ n.text }}
            </v-list-item-title>
          </v-list-item>
        </template>
      </v-list>

      <template #append>
        <div class="pa-2">
          <v-btn
            block
            min-height="45"
            depressed
            color="primary"
            rounded
            class="font-weight-light text-capitalize"
            >Our Services</v-btn
          >
        </div>
      </template>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      nav: [
        { text: "Reviews", link: "/#reviews" },
        { text: "Products", link: "/#products" },
        { text: "Gallery", link: "/#gallery" },
        { text: "About Us", link: "/#about-us" },
        { text: "Contact Us", link: "/#contact-us" },
      ],
    };
  },
};
</script>

<style></style>
