<template>
  <div
    class="subscribe_container d-flex flex-column align-center justify-center"
  >
    <div class="dont_worry_text">
      Don't worry, reading books won't make you regret.
    </div>
    <div class="d-flex align-center">
      <v-text-field
        v-model="search"
        label="Input your email here..........."
        variant="solo"
        class="email_box"
      ></v-text-field>
      <v-btn class="sub_btn">Subscribe Now</v-btn>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: '',
    }
  },
}
</script>

<style scoped>
.subscribe_container {
  padding-bottom: 10rem;
  padding-top: 3rem;
  background-color: rgb(144, 63, 220);
}

.dont_worry_text {
  font-size: clamp(1rem, 3.5vw, 2rem);
  color: white;
  font-weight: 600;
  margin: 2rem 0;
}

.email_box {
  max-width: 80%;
  width: 80%;
  margin: 1rem 0;
}

.sub_btn {
  margin-bottom: 20px;
  margin-left: 20px;
  height: 60px;
  text-transform: capitalize;
  font-weight: 800;
  letter-spacing: 0.7px;
  border: 3px solid black;
  background-color: rgb(244, 215, 52);
}

@media (min-width: 768px) {
  .email_box {
    max-width: 400px;
    width: 400px;
  }
}
</style>

<style>
.email_box .v-field__field {
  border: 3px solid;
  border-radius: 2px;
}
</style>
