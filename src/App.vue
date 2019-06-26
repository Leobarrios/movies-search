<template>
  <div>
    <Navbar v-on:search-movie-title="searchMovie"></navbar>
    <Content v-bind:movie-title="movieTitleToSearch"></Content>
  </div>
</template>




<script>
import Navbar from "./components/Navbar.vue"
import Content from "./components/Content.vue"
// import List from "./components/List.vue"

export default {
  name: "app",
  components: {
    Navbar,
    Content
    // List,
  },
  data() {
    return {
      titulo: 'my movies app',
      movieTitleToSearch: ''
    }
  },
  methods : {
    searchMovie: function (title) {
      this.movieTitleToSearch = title
    }
  }

};
</script>
