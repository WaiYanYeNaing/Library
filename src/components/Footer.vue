<template>
  <div>
    <footer class="sticky-footer d-flex align-center">
      <img
        :src="require('../assets/casual-life-3d-pink-book-in-air.png')"
        class="book_img mx-4"
      />
      <div class="info">
        Find good books herer that will make you beautiful <br />
        and make your brain feel comfortable when you read them
      </div>
      <v-spacer />
      <div>@2023 Copyright WYYN</div>
    </footer>
  </div>
</template>

<style scoped>
.sticky-footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 100px;
  padding: 40px 60px;
  color: aliceblue;
  background-color: rgb(10, 10, 28);
}
.book_img {
  width: 80px;
  height: 60px;
}
.info {
  font-size: 16px;
  letter-spacing: 1px;
}
@media (max-width: 600px) {
  .sticky-footer {
    display: none !important;
  }
}
</style>
