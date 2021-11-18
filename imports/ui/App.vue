<template>
  <div class="container">
    <div class="nav" v-show="login">
      <Navbar
        v-for="element in elements1"
        :key="element._id"
        :element="element"
      />
    </div>
    <div class="nav" v-show="!login">
      <Navbar
        v-for="element in elements2"
        :key="element._id"
        :element="element"
      />
    </div>
    <div v-if="navid==='home'"></div>
    <div v-else-if="navid==='myTransactions'"></div>
    <div v-else-if="navid==='intiateTransactions'"></div>
    <div v-else></div>
  </div>
</template>

<script>
  import Navbar from "./components/Navbar.vue"
  import Loginnav from "./components/Navbar.vue"
  import "./assets/styles.css"
  export default {
      components: {
        Navbar,
      },
      data : {
          login: true,
          navid: "home",
          elements1:  [
          { _id: 1, text: "Home" },
          { _id: 2, text: "My Transactions" },
          { _id: 3, text: "Initiate Transaction"},
          { _id: 4, text: "My Profile"},
          { _id: 5, text: "Logout"}
        ],
        elements2: [
        { _id: 1, text: "Home" },
        { _id: 2, text: "Login"}
      ],
      },
      methods: {},
  };
</script>
