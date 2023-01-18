<template>
  <v-container>
    <v-responsive>
      <header class="d-flex align-center justify-center text-center">
        <h1 class="d-flex align-center my-3">
          Books
          <img
            :src="
              require('../../assets/casual-life-3d-open-orange-book-floating.png')
            "
            class="book_img mx-4"
          />
          Make Your Eyes Bright.
        </h1>
      </header>
    </v-responsive>
    <v-responsive>
      <main class="d-flex align-center justify-center text-center">
        <p class="mb-4">
          Find good clothes here that will make you beautiful and make <br />
          your skin feel comfortable when you wear them
        </p>
      </main>
    </v-responsive>
  </v-container>
</template>

<style scoped>
.book_img {
  width: 70px;
}
h1 {
  font-size: clamp(2rem, 3.5vw, 3rem);
}
</style>
