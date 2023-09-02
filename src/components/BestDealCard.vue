<script>
import ProductCardContent from './ProductCardContent.vue'
</script>

<script setup>
const props = defineProps({
  productImgPath: String,
  productName: String,
  productDescription: String,
  productReviewAverage: Number,
  productTotalReviews: Number,
  productPrice: Number
})

const imageUrl = new URL(`/src/assets/images/${props.productImgPath}`, import.meta.url).href
</script>

<template>
  <div class="best-deal-item-wrap">
    <div class="best-deal-thumbnail">
      <img class="shop-category-image" :src="imageUrl" />
      <div class="product-wishlist">
        <img class="wishlist-icon" src="../assets/wishlist.svg" />
      </div>
    </div>
    <ProductCardContent />
  </div>
</template>

<style scoped>
.product-wishlist {
  position: absolute;
  left: auto;
  top: 16px;
  right: 16px;
  bottom: auto;
  display: flex;
  width: 40px;
  height: 40px;
  justify-content: center;
  align-items: center;
  border-radius: 100px;
  background-color: #fff;
}
.best-deal-thumbnail {
  position: relative;
  background-color: #f5f6f6;
  border-radius: 10px;
  text-align: center;
}

.best-deal-item-wrap {
  margin-right: 10px;
}
</style>
