<template>
  <div class="navli">{{ this.element.text }}</div>
</template>

<script>
  export default {
      props: ["element","url"],
      data() {
      return {};
  }
};
</script>