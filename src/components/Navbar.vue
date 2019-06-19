<template>
    <div>
<nav class="navbar navbar-light bg-light">
  <form class="form-inline" v-on:submit="saludar"> 
     <!-- v-on para eventos -->
    <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
    <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
  </form>
</nav>
    </div>
</template>

methods: {
  saludar: {
    console.log("hola");
  }, 
}


