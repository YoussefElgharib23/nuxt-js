<template>
  <div>
    <Navbar />
    <div class="container">
      <LargeCardDisplay
        v-for="cardInfo in largeCardSections.slice(0, 1)"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/static/data.js";
export default {
  data() {
    return {
      largeCardSections,
      smallCardSections,
    };
  },
  head: {
    title: "Products page",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "Products of fire extinguisher",
      },
    ],
  },
};
</script>

<style scoped>
</style>