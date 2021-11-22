<template>
  <div>
      <h1>Welcome to BankSafe Banking solutions!</h1>
      <p>We are India's first blockhain banking solution. With us on your side, be rest assured your data is absolutely safe.
        Your transactions are now, safer, faster and you may now bid goodbye to all the transaction costs.
      </p>
      <div class="counter-div">
        <div class="counter">
          <h2 @load="runner" id="countrunner">{{count}}</h2>
          <div>Happy customers</div>
        </div>
        <div class="counter">
          <h2>0</h2>
          <div>Cases of data theft</div>
        </div>
      </div>
      <br>
      <h1>Our Services</h1>
      <div class="card-deck">
        <div class="card">
          <h2>Know how we work</h2>
          <p>We take you data security very seriously, click here to read more about how we store your data</p>
        </div>
        <div class="card">
          <h2>Know how we work</h2>
          <p>We take you data security very seriously, click here to read more about how we store your data</p>
        </div>
        <div class="card">
          <h2>Know how we work</h2>
          <p>We take you data security very seriously, click here to read more about how we store your data</p>
        </div>
      </div>
  </div>
</template>

<script>
  export default {
      props: [],
      data() {
      return {count:0};
  },
  methods:{
    runner(){  
      // setInterval(function(){
      //               if(count<3000)
      //                 this.count+=1;
      //               else
      //                 clearInterval(count);
      // },500);
      //write runner code
    }
    }
  };
</script>