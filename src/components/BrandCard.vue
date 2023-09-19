<script></script>

<script setup>
const props = defineProps({
  brandTitle: String,
  brandImgPath: String
})

const imageUrl = new URL(`/src/assets/images/${props.brandImgPath}`, import.meta.url).href
</script>

<template>
  <div class="brand-item">
    <div class="brand-image-wrap">
      <img class="brand-image" :src="imageUrl" />
    </div>
    <div class="brand-content">
      <h3 class="brand-item-title">{{ brandTitle }}</h3>
      <div class="delivery-time">Delivery with in 24 hours</div>
    </div>
  </div>
</template>

<style scoped>
.brand-item {
  position: relative;
  z-index: 0;
  display: flex;
  padding: 20px;
  justify-content: flex-start;
  align-items: center;
  background-color: #f5f6f6;
  border-radius: 10px;
}

.brand-image-wrap {
  position: relative;
  margin-right: 18px;
}

.brand-image {
  border-radius: 10px;
  max-width: 100%;
}

.brand-item-title {
  margin-top: 0px;
  margin-bottom: 13px;
  font-family: Inter, sans-serif;
  color: #231f1e;
  font-size: 18px;
  font-weight: 600;
}

.delivery-time {
  margin-bottom: 0px;
  font-size: 13px;
  line-height: 13px;
  font-weight: 500;
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
