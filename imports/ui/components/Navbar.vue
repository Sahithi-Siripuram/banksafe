<template>
  <div class="navli" @click="display">{{ this.element.text}}</div>
</template>

<script>
import Login from "./Login.vue"
  export default {
     components: {
        Login,
     },
      props: ["element","navid","login"],
      data() {
      return {};
  },
  methods:{
    display(){
      if(this.element._id===1)
        this.$emit('update:navid',"home");
      else if(this.element._id===2)
        this.$emit('update:navid',"myTransactions");
      else if(this.element._id===3)
        this.$emit('update:navid',"intiateTransaction");
      else if(this.element._id===4)
        this.$emit('update:navid',"myProfile");
      else if(this.element.text==="Logout")
          this.$emit('update:login',!this.login);
      // else
      //   <Login/>
    }
  }
};
</script>