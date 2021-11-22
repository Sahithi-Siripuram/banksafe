<template>
  <div>
    <div class="nav" v-show="login">
      <Navbar
        v-for="element in elements1"
        :key="element._id"
        :element="element"
        :login = "login"
        :navid="navid"
        v-on:update:login="login=$event"
        v-on:update:navid="navid=$event"
      />
    </div>
    <div class="nav" v-show="!login">
      <Navbar
        v-for="element in elements2"
        :key="element._id"
        :element="element"
        :login = "login"
        :navid="navid"
        v-on:update:login="login=$event"
        v-on:update:navid="navid=$event"
      />
    </div>
    <div class="body">
      <div v-if="navid==='home'"><Home/></div>
      <div v-else-if="navid==='myTransactions'"><h1>History</h1></div>
      <div v-else-if="navid==='intiateTransaction'"><h1>New Transaction</h1></div>
      <div v-else><h1>My profile</h1></div>
    </div>
    <div class="footer"><Footer/></div>
  </div>
</template>

<script>
  import Navbar from "./components/Navbar.vue"
  import Home from "./components/Home.vue"
  import Footer from "./components/Footer.vue"
  import "./assets/styles.css"
  export default {
      components: {
        Navbar,
        Home,
        Footer,
      },
      data () {
          return{
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
                  { _id: 5, text: "Login / Signup"}
            ],
          }; 
      },
      methods: {},
  };
</script>
