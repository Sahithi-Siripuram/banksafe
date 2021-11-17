<template>
  <li>{{ this.element.text }}</li>
</template>

<script>
  export default {
      props: ["element","url"],
      data() {
      return {};
  }
};
</script>