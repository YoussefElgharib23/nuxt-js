<template>
  <NuxtLink :to="`/products/${card.id}`" class="card-container">
    <img
      :data-src="require(`@/static/images/${card.image || 'fe1.jpg'}`)"
      alt="Extinguisher image"
      class="image"
      v-lazy-load
    />
  </NuxtLink>
</template>
<script>
export default {
  props: {
    card: Object,
  },
};
</script>
<style scoped>
.card-container {
  width: 24%;
  height: 12.5rem;
  border-radius: 0.5rem;
  overflow: hidden;
  margin-bottom: 1.5rem;
  cursor: pointer;
}
.image {
  width: 100%;
  height: 100%;
}
</style>