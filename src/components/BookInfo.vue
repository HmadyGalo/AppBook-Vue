<script>
export default {
  data() {
    return {
      detailAreVisible: false,
      books: 
        {
          id: 1,
          title: "Narnia",
          author: "C.S Lewis",
          releaseDate: "1999-12-02",
        },
      
    };
  },
  methods: {
    togleDetails() {
      this.detailAreVisible = !this.detailAreVisible;
    },
  },
};
</script>

<template>
  <li>
    <h2>{{ books.title }}</h2>
    <button type="button" @click="togleDetails">
      {{ detailAreVisible ? "Hide" : "Show" }}
    </button>
    <ul v-if="detailAreVisible">
      <li><strong>Autor: </strong> {{ books.author }}</li>
      <li><strong>Release Date: </strong>{{ books.releaseDate }}</li>
    </ul>
  </li>
</template>
