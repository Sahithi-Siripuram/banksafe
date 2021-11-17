<template>
  <div class="container">
    <div class="nav">
      <Navbar
        v-for="element in getElements()"
        :key="element._id"
        :element="element"
        :href="url"
      />
    </div>
    <header>
      <h1>Todo List</h1>
    </header>
  </div>
</template>

<script>
  import Navbar from "./components/Navbar.vue"
  import "./assets/styles.css"
  export default {
      components: {
        Navbar
      },
      data() {
          return {};
      },
      methods: {
      getElements() {
      return [
        { _id: 1, text: "Home" , url: "google.com"},
        { _id: 2, text: "My Transactions", url: "google.com" },
        { _id: 3, text: "Initiate Transaction", url: "google.com" },
        { _id: 4, text: "My Profile", url: "google.com" }
      ];
    }
  }
};
</script>
