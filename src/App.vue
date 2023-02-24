<script>
export default {
  data() {
    return {
      books: [
        {
          id: 1,
          title: "Narnia",
          author: "C.S Lewis",
          releaseDate: "1999-12-02",
        },
        {
          id: 2,
          title: "Narnia II",
          author: "C.S Lewis",
          releaseDate: "1999-12-02",
        },
        {
          id: 3,
          title: "Narnia III",
          author: "C.S Lewis",
          releaseDate: "1999-12-02",
        },
      ],
    };
  },
};
</script>

<template>
  <h1>My Books</h1>
  <ul>
    <book-info></book-info>
    <book-info></book-info>
    <book-info></book-info>
  </ul>
</template>
<style>
h1 {
  color: aqua;
}
</style>
