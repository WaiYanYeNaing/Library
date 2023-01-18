<template>
  <div class="booksList_container">
    <div class="search-container d-flex justify-center">
      <v-text-field
        v-model="search"
        label="Search for a book"
        variant="solo"
        density="compact"
        class="search_box"
      ></v-text-field>
    </div>
    <v-row class="books_continer">
      <v-col
        cols="12"
        md="6"
        lg="4"
        v-for="book in filteredBooks"
        :key="book.id"
        class="d-flex justify-center"
      >
        <v-card
          class="elevation-4 d-flex flex-column align-center"
          @click="navigateToAboutPage(book.url)"
          v-transition="{ name: 'fade', mode: 'out-in' }"
        >
          <img :src="book.image" class="card_image" />
          <v-card-title>{{ book.title }}</v-card-title>
          <v-card-subtitle>{{ book.author }}</v-card-subtitle>
          <v-card-text>{{ book.description }}</v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: '',
      books: [
        {
          id: 1,
          title: 'Harry Potter',
          author: 'J.K. Rowling',
          description: 'A young boy discovers he is a wizard',
          image:
            'https://m.media-amazon.com/images/I/51mFoFmu0EL._SX335_BO1,204,203,200_.jpg',
          url: 'https://hpread.scholastic.com/HP_Book1_Chapter_Excerpt.pdf',
        },
        {
          id: 2,
          title: 'To Kill a Mockingbird',
          author: 'Harper Lee',
          description: 'A story of racial injustice in the south',
          image:
            'https://m.media-amazon.com/images/I/81aY1lxk+9L._AC_UY327_FMwebp_QL65_.jpg',
          url: 'https://www.raio.org/TKMFullText.pdf',
        },
        {
          id: 3,
          title: 'The Great Gatsby',
          author: 'F. Scott Fitzgerald',
          description: 'A tale of wealth and excess in the 1920s',
          image:
            'https://m.media-amazon.com/images/I/61szdrztBtL._AC_UY327_FMwebp_QL65_.jpg',
          url: 'https://www.wsfcs.k12.nc.us/cms/lib/NC01001395/Centricity/Domain/7935/Gatsby_PDF_FullText.pdf',
        },
        {
          id: 4,
          title: 'The Catcher in the Rye',
          author: 'J.D. Salinger',
          description: 'A story of teenage rebellion and alienation',
          image:
            'https://m.media-amazon.com/images/I/71nXPGovoTL._AC_UY327_FMwebp_QL65_.jpg',
          url: 'https://www.uzickagimnazija.edu.rs/files/Catcher%20in%20the%20Rye.pdf',
        },
        {
          id: 5,
          title: 'The Lord of the Rings',
          author: 'J.R.R. Tolkien',
          description: 'A epic fantasy novel of good versus evil',
          image:
            'https://m.media-amazon.com/images/I/91XxVTG9kVL._AC_UY327_FMwebp_QL65_.jpg',
          url: 'https://gosafir.com/mag/wp-content/uploads/2019/12/Tolkien-J.-The-lord-of-the-rings-HarperCollins-ebooks-2010.pdf',
        },
        {
          id: 6,
          title: "The Hitchhiker's Gui....",
          author: 'Douglas Adams',
          description: 'A comedic science fiction series',
          image:
            'https://m.media-amazon.com/images/I/A1fE+AMrKPL._AC_UY327_FMwebp_QL65_.jpg',
          url: 'https://jaydixit.com/files/PDFs/TheultimateHitchhikersGuide.pdf',
        },
        {
          id: 7,
          title: 'The Girl with the Dragon Tattoo',
          author: 'Stieg Larsson',
          description: 'A crime novel about a hacker and a journalist',
          image:
            'https://m.media-amazon.com/images/I/81u348JYT6L._AC_UY327_FMwebp_QL65_.jpg',
          url: 'https://ebooknoid.files.wordpress.com/2012/01/the_girl_with_the_dragon_tattoo.pdf',
        },
        {
          id: 8,
          title: 'The Da Vinci Code',
          author: 'Dan Brown',
          description:
            'A thriller novel with a historical and religious conspiracy',
          image:
            'https://m.media-amazon.com/images/I/81jtrIKJd2L._AC_UY327_FMwebp_QL65_.jpg',
          url: 'https://ia600404.us.archive.org/9/items/TheDaVinciCode_201308/The%20Da%20Vinci%20Code.pdf',
        },
        {
          id: 9,
          title: 'The Hunger Games',
          author: 'Suzanne Collins',
          description:
            'A dystopian novel about a young girl and a deadly competition',
          image:
            'https://m.media-amazon.com/images/I/4134W9qxFIL._AC_UY327_FMwebp_QL65_.jpg',
          url: 'https://books-library.net/files/books-library.online-12251706Mg5J8.pdf',
        },
        {
          id: 10,
          title: 'Gone with the Wind',
          author: 'Margaret Mitchell',
          description:
            'A story of love and survival set in the American Civil War',
          image:
            'https://m.media-amazon.com/images/I/51S96fD6ORL._AC_UY327_FMwebp_QL65_.jpg',
          url: 'https://s3.amazonaws.com/scschoolfiles/112/gone_with_the_wind.pdf',
        },
      ],
    }
  },
  computed: {
    filteredBooks() {
      return this.books.filter((book) =>
        book.title.toLowerCase().includes(this.search.toLowerCase())
      )
    },
  },
  methods: {
    navigateToAboutPage(url) {
      console.log(url)
      this.$router.push({ name: 'about', query: { url } })
    },
  },
}
</script>

<style scoped>
.booksList_container {
  padding-bottom: 6rem;
}
.search_box {
  max-width: 300px;
  margin: 1rem 0;
}
.books_continer {
  max-width: 70vw;
  margin: 0 auto;
}
.v-card {
  border: 2px solid;
  border-radius: 10px;
  min-width: 300px;
  max-width: 300px;
  margin: 10px;
}
.card_image {
  width: 300px;
  height: 350px;
  object-fit: cover;
  object-position: top;
}
</style>

<style>
.search_box .v-field__field {
  background: #ffd667;
  border: 1px solid;
  border-radius: 5px;
}
</style>
