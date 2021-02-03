<template>
  <div>
    <b-navbar toggleable="lg" type="dark">
      <b-navbar-brand to="/">
        <b-avatar rounded variant="light">KH</b-avatar>
        <span class="brand_text">Kyle Hadland</span>
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item
            v-for="item in nav_items"
            :key="item.id"
            :to="item.link"
            >
            <span v-html="item.title"></span>
          </b-nav-item>
          <b-nav-item v-for="item in socials" :key="item.id" :href="item.link">
            <b-icon class="nav_icon" :icon="item.icon"></b-icon>
          </b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
import { BIcon, BIconFacebook, BIconLinkedin } from "bootstrap-vue";

export default {
  components: {
    BIcon,
    BIconLinkedin,
    BIconFacebook,
  },
  data() {
    return {
      nav_items: [
        { link: "/", title: "Home" },
        // { link: "about", title: "About" },
        { link: "resume", title: "Resum&eacute;" },
        { link: "contact", title: "Contact" }
      ],
      socials: [
        { link: "http://au.linkedin.com/in/kylehadland", title: "LinkedIn", icon: "linkedin" },
        { link: "http://www.facebook.com/kyle.hadland/", title: "Facebook", icon: "facebook" },
      ],
    };
  },
  watch: {},
  mounted() {},
  methods: {},
  beforeDestroy() {},
};
</script>

<style scoped>
/*  */
.brand_text {
  text-shadow: 0px 1px 2px rgba(0,0,0,0.7);
  /* text-shadow: 0px 1px 3px #000000; */
  opacity: 0.9;
}
.b-avatar {
  box-shadow: 1px 1px 2px rgba(0,0,0,0.6);
  opacity: 0.8;
  color: rgba(9,9,121,1);
}
.navbar-nav .nav-link {
  color: rgba(255,255,255,0.85);
  text-shadow: 0px 1px 2px rgba(0,0,0,0.7);
  /* box-shadow: 0px 1px 2px rgba(0,0,0,0.7); */
}
.nav_icon {
    filter: drop-shadow( 1px 1px 2px rgba(0, 0, 0, 0.5));
    opacity: 0.85;
}
</style>