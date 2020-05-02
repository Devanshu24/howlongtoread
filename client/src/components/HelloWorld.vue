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
        <h1 class="jaadu">
          HowLongToRead ?
        </h1>
      </v-col>
    </v-row>
    <v-row class="text-center">
      <v-col cols="3"> </v-col>
      <v-col cols="6">
        <v-text-field placeholder="So what's your read?"> </v-text-field>
      </v-col>
      <v-col cols="3"> </v-col>
    </v-row>
    <v-row class="text-center">
      <v-col class="mainContent">
        <h2>
          We have all been wanting to read books! May it be that New Years'
          Resolution or to impress your better half ;)
          <br />
          But we always fear the length of the book, well that has now come to
          an end!
        </h2>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld"
};
</script>

<style scoped>
.mainContent h2 {
  font-family: "Roboto";
  font-weight: 400;
}
.jaadu {
  font-family: "Roboto";
  font-weight: 100;
  font-size: 60px;
}
</style>
