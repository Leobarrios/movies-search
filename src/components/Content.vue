<template>
    <div>
<table class="table">
  <thead>
    <tr>
      <th scope="col">id</th>
      <th scope="col">Name</th>
      <th scope="col">Year</th>
      <th scope="col">Age</th>
    </tr>
  </thead>
  <tbody>
      
    <tr v-for="item in movies" :key="item.id">
      <th scope="row">{{item.id}}</th>
      <td>{{item.name}}</td>
      <td>{{item.year}}</td>
      <td>{{item.age}}</td>
    </tr>
  </tbody>
</table>



    </div>
</template>

<script>
export default {
    name: 'Content',
    props: ['movieTitle'],
    data() {
        return {
            movies: []
    }
  },
  mounted() {
    this.loadCatalog()
  },
  methods: {
    loadCatalog: async function() {
      const data = await fetch('./catalog.json')
      this.movies = await data.json()
    }
  }
}
</script>

