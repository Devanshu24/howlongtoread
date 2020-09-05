<template>
  <div class="notFound">
    <v-img
      :src="require('../assets/notFound.svg')"
      class="my-3 logo404"
      contain
      height="300"
    >
    </v-img>
    <h1 class="text404">
      Error 404 Not Found
    </h1>
  </div>
</template>

<script>
export default {
  name: "notFound"
};
</script>

<style>
.notFound {
  display: grid;
  grid-template-columns: 1fr;
}
.logo404 {
  grid-row: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
.text404 {
  grid-row: 2;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
