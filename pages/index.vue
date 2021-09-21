<template>
  <div>
    <Navbar />
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="cardInfo in largeCardSections"
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
import { largeCardSections } from "@/static/data.js";
import { smallCardSections } from "@/static/data.js";
export default {
  data() {
    return {
      largeCardSections,
      smallCardSections,
    };
  },
};
</script>