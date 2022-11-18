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
      iconList: ["fa-facebook-f", "fa-instagram", "fa-twitter", "fa-youtube"],
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
  <footer>
    <div class="footer-top">
      <img src="./assets/images/avada-charity-sticky-header-logo-retina.png">
    </div>
    <div class="footer-bottom">
      <small>&copy; copyright 2012 - 2020 AVADA THEME BY TEAM FUSION | ALL RIGHTS RESERVED | POWERED BY
        WORDPRESS</small>
      <ul class="icon-list">
        <li class="icon" v-for="(icon, index) in iconList">
          <i class="fa-brands" :class="icon"></i>
        </li>
      </ul>
    </div>
  </footer>

</template>
<style lang="scss">
@use "./style/partials/variables" as *;
@use "./style/general.scss" as *;

.footer-top {
  display: flex;
  justify-content: center;
  padding: 1rem 0;
  background-color: white;

  img {
    height: 50px;
  }
}

.footer-bottom {
  padding: 1rem 0;
  text-align: center;
  color: gray;
  background-color: $bg-foot-bt;

  ul {
    display: flex;
    justify-content: center;
    margin-top: 1.5rem;

    li {
      margin-right: 1.5rem;
      width: 35px;
      height: 35px;
      color: $color-bt;
      border-radius: 50%;
      background-color: white;
      line-height: 35px;
      text-align: center;
    }


  }

}
</style>