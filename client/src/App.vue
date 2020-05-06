<template>
  <v-app>
    <NavBar />
    <div class="router">
      <router-view></router-view>
    </div>
    <Footer class="footer" />
  </v-app>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import Footer from "@/components/Footer.vue";
export default {
  name: "App",
  components: {
    NavBar,
    Footer
  }
};
</script>

<style>
* {
  font-family: 'Roboto';
}
.footer {
  margin-top: 20px;
}
.router {
  padding-top: 100px;
  height: 100%;
}
</style>
