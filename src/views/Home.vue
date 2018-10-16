<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <input v-model="message">

    <div v-for="review in reviews">
      <h2>{{ review.reviewer }} - {{ review.rating }} Stars</h2>
      <p>{{ review.text }}</p>
    </div>

  </div>
</template>

<style>
body {
  background-color: lightblue;
}
</style>

<script>
export default {
  data: function() {
    return {
      message: "Welcome to Vue.js! something",
      reviews: [
        { 
          text: "Vue.js is the best thing since sliced bread!",
          rating: 5,
          reviewer: "Burton Wax"
        },
        { 
          text: "I love Vue.js, especially when I'm programming!",
          rating: 4,
          reviewer: "Emily Post"
        },
        { 
          text: "Vue.js sucks.",
          rating: 1,
          reviewer: "Oscar the Grouch"
        }
      ]
    };
  },
  created: function() {},
  methods: {},
  computed: {}
};
</script>