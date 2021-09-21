<template>
  <div>Hello i have id on route {{ this.$route.params.id }} {{ cards }}</div>
</template>
<script>
export default {
  computed: {
    cards() {
      return this.$store.state.card.list;
    },
  },
  head: {
    title: "Home page",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "Home page description",
      },
    ],
  },
};
</script>
<style>
</style>