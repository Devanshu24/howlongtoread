<template>
  <v-app>
    <v-app-bar
      app
      :collapse-on-scroll="false"
      absolute
      flat
      :color="color.primary"
      dark
    >
      <!-- https://codesandbox.io/embed/14ry9r3lll RESPONSIVE APP BAR -->
      <div class="d-flex align-center">
        <v-img
          alt="Logo"
          class="shrink mr-2"
          contain
          src="./assets/time.svg"
          transition="scale-transition"
          width="80"
          @click="changeIcon"
        />
        <!-- <h1 class="title">
          HowLongToRead
        </h1> -->
        <v-toolbar-title>HowLongToRead</v-toolbar-title>
      </div>

      <v-spacer></v-spacer>
      <v-btn text @click="changeIcon" v-if="iconState == 'Bright'">
        <v-icon>
          mdi-brightness-7
        </v-icon>
      </v-btn>
      <v-btn text @click="changeIcon" v-if="iconState == 'Dark'">
        <v-icon>
          mdi-brightness-4
        </v-icon>
      </v-btn>
      <v-btn text>
        <v-icon color="white">fab fa-goodreads</v-icon>
        <span class="ml-2">Login</span>
        <!-- <i class="fas fa-sign-in-alt"></i> -->
      </v-btn>
    </v-app-bar>

    <v-content>
      <HelloWorld />
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    HelloWorld
  },
  data: () => ({
    color: {
      primary: "#63C3FF",
      secondary: "#63F3FF"
    },
    iconState: "Dark"
    //
  }),
  methods: {
    changeIcon() {
      if (this.iconState === "Bright") {
        this.iconState = "Dark";
        const temp = this.color.primary;
        this.color.primary = this.color.secondary;
        this.color.secondary = temp;
      } else {
        this.iconState = "Bright";
        const temp = this.color.primary;
        this.color.primary = this.color.secondary;
        this.color.secondary = temp;
      }
    }
  }
};
</script>

<style>
.title {
  font-family: "Roboto";
}
</style>
