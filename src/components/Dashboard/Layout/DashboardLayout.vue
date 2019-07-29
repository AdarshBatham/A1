<template>
  <div class="wrapper">
   
    <div class="main-panel">
      <top-bar></top-bar>
      <!-- <top-navbar></top-navbar> -->

      <dashboard-content @click="toggleSidebar">
      </dashboard-content>

      <content-footer></content-footer>
    </div>
  </div>
</template>

<style lang="scss">
</style>

<script>
  // import TopNavbar from './TopNavbar.vue'
  import TopBar from './TopBar.vue'
  import ContentFooter from './ContentFooter.vue'
  import DashboardContent from './Content.vue'
  import MobileMenu from './MobileMenu.vue'
  export default {
    components: {
      // TopNavbar,
      TopBar,
      ContentFooter,
      DashboardContent,
      MobileMenu
    },
    methods: {
      toggleSidebar () {
        if (this.$sidebar.showSidebar) {
          this.$sidebar.displaySidebar(false)
        }
      }
    }
  }

</script>
