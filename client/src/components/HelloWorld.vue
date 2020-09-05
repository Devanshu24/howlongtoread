// color: #63F3FF
<template>
  <v-container>
    <v-row class="text-center mt-4">
      <v-img
        :src="require('../assets/home.svg')"
        class="my-3"
        contain
        height="300"
      >
      </v-img>
    </v-row>
    <v-row class="text-center">
      <v-col>
        <h1>
          HowLongToRead?
        </h1>
      </v-col>
    </v-row>
    <div class="search">
      <v-text-field ref="search" placeholder="So what's your read?" />
    </div>
    <div class="mainContent">
      We have all been wanting to read books! May it be that New Years'
      Resolution or to impress your better half ;)
    </div>
    <div class="mainContent">
      But we always fear the length of the book, well that has now come to an
      end!
    </div>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",
  mounted() {
    this.focusInput();
  },
  methods: {
    focusInput() {
      this.$refs.search.focus();
    }
  }
};
</script>

<style scoped>
.mainContent {
  display: flex;
  justify-content: center;
  width: 100%;
  font-size: 120%;
}
.jaadu {
  font-family: "Roboto";
  font-weight: 100;
  font-size: 60px;
}
.search {
  display: flex;
  justify-content: center;
  width: 100%;
  padding-left: 20%;
  padding-right: 20%;
}
</style>
