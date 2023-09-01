<script></script>

<script setup>
const props = defineProps({
  categoryTitle: String,
  categoryImgPath: String
})

const imageUrl = new URL(`/src/assets/images/${props.categoryImgPath}`, import.meta.url).href
</script>

<template>
  <div class="shop-category-item">
    <img class="shop-category-image" :src="imageUrl" />
    <h3 class="shop-category-item-title">{{ categoryTitle }}</h3>
  </div>
</template>

<style scoped>
.shop-category-item {
  position: relative;
  z-index: 0;
  overflow: hidden;
  border-radius: 10px;
}

.shop-category-image {
  border-radius: 10px;
  max-width: 100%;
  vertical-align: middle;
  display: inline-block;
}

.shop-category-item-title {
  position: absolute;
  left: 0%;
  top: 0%;
  right: auto;
  bottom: auto;
  z-index: 1;
  width: 100%;
  color: #fff;
  font-size: 24px;
  font-weight: 600;
  text-align: center;
}

h3 {
  margin-top: 20px;
  margin-bottom: 10px;
  font-family: Eina02, sans-serif;
  font-size: 28px;
  line-height: 100%;
  font-weight: 700;
}
</style>
