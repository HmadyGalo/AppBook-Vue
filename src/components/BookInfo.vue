<script>
export default {
 // props: ["id", "title","author","releaseDate","isLiked"],
 //objeto valida props
 props:{
  id:{
    type:String,
    required:true,
  },
  title:{
    type:String,
    required:true,
  },
  author:{
    type:String,
    required:true,
  },
  releaseDate:{
    type:String,
    required:true,
  },
  isLiked:{
    type:String,
    required:false,
    default:"0",
    validator: function(value){
      return value === "1"|| value ==="0"
    }
  },
 },

  data() {
    return {
      detailAreVisible: false,
      bookIsLiked:this.isLiked,
     
    };
  },
  methods: {
    toggleDetails() {
      this.detailAreVisible = !this.detailAreVisible;
    },
    toggleFavorite(){
      if ( this.bookIsLiked==="1") {
        this.bookIsLiked="0"
      } else {
        this.bookIsLiked="1"
      }

    },
  },
};
</script>

<template>
  <li>
    <h2>{{ title }} {{ bookIsLiked==="1" ? "(Liked)" : "(Not Liked)"}}</h2>
    <button type="button" @click="toggleDetails">
      {{ detailAreVisible ? "Hide" : "Show" }}
    </button>
    <button type="button" @click="toggleFavorite">
Toggle Favorite
    </button>
    <ul v-if="detailAreVisible">
      <li><strong>Autor: </strong> {{ author }}</li>
      <li><strong>Release Date: </strong>{{ releaseDate }}</li>
    </ul>
  </li>
</template>
