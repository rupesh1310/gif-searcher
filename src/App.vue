
<template>
  <div id="app">
    <h1>Amazing Gif Searcher</h1>
    <input v-model="searchTerm" type="text">
    <button class="button" @click=getGifs()>Search</button>
    <div class="gif-container">
      <img v-for="gif in gifs" :src="gif" :key="gif.id">
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      searchTerm: ""
    };
  },
  methods: {
    getGifs() {
      console.log(this.searchTerm);
    }
  }
};
</script>


<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
input {
  padding: 5px;
  margin-bottom: 20px;
}

.button {
  background-color: rgb(0, 172, 0);
  color: white;
  padding: 5px 20px;
  border: none;
  display: block;
  margin: 0 auto;
}

.button:hover {
  background-color: rgb(0, 148, 0);
}
</style>