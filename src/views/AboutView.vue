<template>
  <div class="about">
    <object :data="url" type="application/pdf" class="pdf">
      <div>No online PDF viewer installed</div>
    </object>
  </div>
</template>

<script>
export default {
  computed: {
    url() {
      console.log(this.$route.query.url)
      return this.$route.query.url
    },
  },
}
</script>

<style scoped>
.pdf {
  width: 100vw;
  height: 92vh;
}
</style>
