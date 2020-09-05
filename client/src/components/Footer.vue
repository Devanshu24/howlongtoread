<template>
  <v-footer dark padless>
    <v-card
      flat
      tile
      class="lighten-1 white--text wrapper"
      :color="color.primary"
    >
      <!-- <v-card-text class="one">
        <v-btn v-for="icon in icons" :key="icon" class="mx-4 white--text" icon>
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text> -->
      <v-card-text class="white--text p-0 two">
        A
        <strong style="margin: 0px 10px 0px 10px">
          <a href="https://github.com/Devanshu24" class="itsme">
            think__tech
          </a>
        </strong>
        Creation
      </v-card-text>
      <v-divider></v-divider>
      <v-card-text class="white--text three">
        {{ new Date().getFullYear() }} —
        <strong>
          HowLongToRead
        </strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  data: () => ({
    icons: ["mdi-facebook", "mdi-github", "mdi-linkedin", "mdi-instagram"],
    color: {
      primary: "#005890",
      secondary: "#63F3FF",
      tertiary: "#63C3FF"
    }
  })
};
</script>
<style scoped>
.wrapper {
  display: grid;
  grid-template-columns: 100vw;
  grid-gap: 10px;
  grid-template-rows: 70px;
}
/* .one {
  grid-row: 1;
  display: flex;
  justify-content: center;
  align-items: center;
} */
.two {
  grid-row: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
.three {
  grid-row: 2;
  display: flex;
  justify-content: center;
  align-items: center;
}
.itsme {
  text-decoration: none;
  color: inherit;
}
</style>
