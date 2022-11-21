<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },
  data() {
    return {
      iconLink: ["fa-facebook-f", "fa-instagram", "fa-twitter", "fa-youtube"],
      links: [
        {
          title: "Home",
          href: "index.html",
          active: true,
        },
        {
          title: "Mission",
          href: "mission.html",
          active: false
        },
        {
          title: "Causes",
          href: "Causes.html",
          active: false
        },
        {
          title: "Journal",
          href: "Journal.html",
          active: false
        },
        {
          title: "Donate",
          href: "index.html",
          active: false
        },





      ]
    }
  }
}
</script>
<template>
  <AppHeader :listLinks="links" />
  <AppMain />
  <AppFooter :iconList="iconLink" />


</template>
<style lang="scss">
@use "./style/partials/variables" as *;
@use "./style/general.scss" as *;
</style>