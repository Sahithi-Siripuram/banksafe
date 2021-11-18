<template>
  <div class="navli" @click="display">{{ this.element.text}}</div>
</template>

<script>
  export default {
      props: ["element"],
      data() {
      return {};
  },
  methods:{
    
  }
};
</script>