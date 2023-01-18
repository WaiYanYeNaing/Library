<template>
  <v-toolbar>
    <!-- <v-btn depressed to="/">Home</v-btn>
    <v-btn depressed to="/about">About</v-btn> -->
    <div class="title d-flex" @click="navigateToHomePage">
      Library
      <img
        src="https://img.icons8.com/avantgarde/100/null/repository.png"
        class="book_img"
      />
    </div>
    <v-spacer />
    <v-toolbar-title class="text-uppercase"
      ><img
        src="https://img.icons8.com/dusk/44/null/circled-user-male-skin-type-3.png"
    /></v-toolbar-title>
    <!-- <v-btn text to="/contact">Contact</v-btn> -->
  </v-toolbar>
</template>

<script>
export default {
  methods: {
    navigateToHomePage() {
      this.$router.push({ name: 'home' })
    },
  },
}
</script>

<style scoped>
.title {
  margin-left: 2rem;
  font-size: 20px;
  font-weight: 700;
}
.book_img {
  width: 30px;
}
.v-toolbar {
  background-color: rgb(234, 230, 198);
}
.v-btn {
  color: black !important;
}
.v-toolbar-title {
  max-width: 70px !important;
}
</style>
