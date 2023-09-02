<script></script>

<script setup>
import AddCartButton from './Buttons/AddCartButton.vue'
</script>

<template>
  <div class="product-content">
    <div class="product-title-wrap">
      <h3 class="product-title">HomePod mini</h3>
      <div class="product-price">
        <span class="text-span">$</span>239<span class="text-span">.00</span>
      </div>
    </div>
    <div class="product-description-wrap">Table with air purifier, stained veneer/black</div>
    <div class="product-rating-wrap">
      <div class="star-wrap">
        <img class="rating-star" src="../assets/rating_star.svg" />
        <img class="rating-star" src="../assets/rating_star.svg" />
        <img class="rating-star" src="../assets/rating_star.svg" />
        <img class="rating-star" src="../assets/rating_star.svg" />
        <img class="rating-star" src="../assets/rating_star.svg" />
      </div>
      <div class="total-rating">(121)</div>
    </div>
    <div class="product-button-wrap"><AddCartButton /></div>
  </div>
</template>

<style scoped>
.product-button-wrap {
  display: inline-block;
}
.text-span {
  position: relative;
  top: -5px;
  font-size: 13px;
}
.total-rating {
  margin-left: 5px;
  font-size: 12px;
  line-height: 100%;
  font-weight: 500;
}

.rating-star {
  width: 14px;
  margin-right: 2px;
}
.star-wrap {
  line-height: 14px;
}

.product-rating-wrap {
  display: flex;
  align-items: center;
  margin-bottom: 12px;
}
.product-description-wrap {
  margin-bottom: 10px;
  font-size: 12px;
  line-height: 16.5px;
  font-weight: 300;
}

.product-price {
  font-weight: 700;
  font-size: 18px;
}

.product-title {
  margin-top: 16px;
  margin-bottom: 12px;
  color: #231f1e;
  font-size: 18px;
  font-weight: 600;
}
.product-title-wrap {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
