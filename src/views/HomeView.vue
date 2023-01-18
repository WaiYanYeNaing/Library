<template>
  <Header />
  <BooksList />
  <Subscribe />
</template>

<script>
import Header from '@/components/Home/Header.vue'
import BooksList from '@/components/Home/BooksList.vue'
import { defineComponent } from 'vue'
import Subscribe from '@/components/Home/Subscribe.vue'

export default defineComponent({
  name: 'HomeView',

  components: {
    Header,
    BooksList,
    Subscribe,
  },
})
</script>
