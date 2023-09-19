<script setup>
import CategoryCard from './components/CategoryCard.vue'
import HeroBanner from './components/HeroBanner.vue'
import Navbar from './components/navbar/Navbar.vue'
import BestDealCard from './components/BestDealCard.vue'
import BrandCard from './components/BrandCard.vue'
</script>

<script>
export default {
  data() {
    return {
      categories: [
        {
          categoryId: 1,
          categoryTitle: 'Furniture',
          categoryImgPath: 'cat_furniture.png'
        },
        {
          categoryId: 2,
          categoryTitle: 'Hand Bag',
          categoryImgPath: 'cat_hand_bag.png'
        },
        {
          categoryId: 3,
          categoryTitle: 'Books',
          categoryImgPath: 'cat_books.png'
        },
        { categoryId: 4, categoryTitle: 'Tech', categoryImgPath: 'cat_tech.png' },
        {
          categoryId: 5,
          categoryTitle: 'Sneakers',
          categoryImgPath: 'cat_sneakers.png'
        },
        {
          categoryId: 6,
          categoryTitle: 'Travel',
          categoryImgPath: 'cat_travel.png'
        }
      ],
      bestDeals: [
        {
          productId: 1,
          productImgPath: 'bestdeal-1.png',
          productName: 'HomePod mini',
          productDescription: 'Table with air purifier, stained veneer/black',
          productReviewAverage: 4.5,
          productTotalReviews: 121,
          productPrice: 239
        },
        {
          productId: 2,
          productImgPath: 'bestdeal-1.png',
          productName: 'HomePod mini',
          productDescription: 'Table with air purifier, stained veneer/black',
          productReviewAverage: 4.5,
          productTotalReviews: 121,
          productPrice: 239
        },
        {
          productId: 2,
          productImgPath: 'bestdeal-1.png',
          productName: 'HomePod mini',
          productDescription: 'Table with air purifier, stained veneer/black',
          productReviewAverage: 4.5,
          productTotalReviews: 121,
          productPrice: 239
        },
        {
          productId: 2,
          productImgPath: 'bestdeal-1.png',
          productName: 'HomePod mini',
          productDescription: 'Table with air purifier, stained veneer/black',
          productReviewAverage: 4.5,
          productTotalReviews: 121,
          productPrice: 239
        },
        {
          productId: 2,
          productImgPath: 'bestdeal-1.png',
          productName: 'HomePod mini',
          productDescription: 'Table with air purifier, stained veneer/black',
          productReviewAverage: 4.5,
          productTotalReviews: 121,
          productPrice: 239
        },
        {
          productId: 2,
          productImgPath: 'bestdeal-1.png',
          productName: 'HomePod mini',
          productDescription: 'Table with air purifier, stained veneer/black',
          productReviewAverage: 4.5,
          productTotalReviews: 121,
          productPrice: 239
        },
        {
          productId: 2,
          productImgPath: 'bestdeal-1.png',
          productName: 'HomePod mini',
          productDescription: 'Table with air purifier, stained veneer/black',
          productReviewAverage: 4.5,
          productTotalReviews: 121,
          productPrice: 239
        }
      ],
      brands: [
        {
          brandId: 1,
          brandTitle: 'Staples',
          brandImgPath: 'brand_staples.png'
        },
        {
          brandId: 2,
          brandTitle: 'Sprouts',
          brandImgPath: 'brand_sprouts.png'
        },
        {
          brandId: 3,
          brandTitle: 'Grocery outlet',
          brandImgPath: 'brand_grocery_outlet.png'
        },
        {
          brandId: 3,
          brandTitle: 'Grocery outlet',
          brandImgPath: 'brand_grocery_outlet.png'
        },
        {
          brandId: 3,
          brandTitle: 'Grocery outlet',
          brandImgPath: 'brand_grocery_outlet.png'
        },
        {
          brandId: 3,
          brandTitle: 'Grocery outlet',
          brandImgPath: 'brand_grocery_outlet.png'
        },
        {
          brandId: 3,
          brandTitle: 'Grocery outlet',
          brandImgPath: 'brand_grocery_outlet.png'
        },
        {
          brandId: 3,
          brandTitle: 'Grocery outlet',
          brandImgPath: 'brand_grocery_outlet.png'
        }
      ]
    }
  }
}
</script>
<template>
  <Navbar />
  <HeroBanner />
  <section class="shop-category-area">
    <div class="container">
      <div class="category-title-wrap">
        <h3 class="categories-title">Shop our top categories</h3>
      </div>
      <div class="shop-category-wrap">
        <CategoryCard
          v-for="(item, index) in categories"
          :item="item"
          :index="index"
          :key="item.categoryId"
          :categoryTitle="item.categoryTitle"
          :categoryImgPath="item.categoryImgPath"
        />
      </div>
    </div>
  </section>

  <section class="best-deal-area">
    <div class="container">
      <div class="best-deal-title-wrap">
        <h3 class="best-deal-title">Todays best deals for you!</h3>
      </div>
      <div class="best-deal-wrap">
        <div class="best-deal-slider">
          <BestDealCard
            class="best-deal-slide"
            v-for="(item, index) in bestDeals"
            :item="item"
            :index="index"
            :key="item.productId"
            :productImgPath="item.productImgPath"
            :productName="item.productName"
            :productDescription="item.productDescription"
            :productReviewAverage="item.productReviewAverage"
            :productTotalReviews="item.productTotalReviews"
            :productPrice="item.productPrice"
          />
        </div>
      </div>
    </div>
  </section>

  <section class="brand-area">
    <div class="container">
      <div class="brand-title-wrap">
        <h3 class="brand-title">Choose By Brand</h3>
      </div>
      <div class="brand-wrap">
        <BrandCard
          v-for="(item, index) in brands"
          :item="item"
          :index="index"
          :key="item.brandId"
          :brandTitle="item.brandTitle"
          :brandImgPath="item.brandImgPath"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.brand-wrap {
  display: grid;
  flex-wrap: nowrap;
  grid-auto-columns: 1fr;
  grid-column-gap: 23px;
  grid-row-gap: 16px;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-rows: auto;
}

.best-deal-area {
  padding-bottom: 80px;
}
.best-deal-slider .best-deal-slide {
  flex-shrink: 0;
  scroll-snap-align: center;
}

.best-deal-slider .best-deal-slide:last-child {
  padding-right: 20px;
}

.best-deal-slider {
  display: flex;
  /* -ms-overflow-style: none; */
  scrollbar-width: none;
  width: auto;
  overflow-y: hidden;
  overflow-x: scroll;
  display: flex;
  align-items: stretch;
  scroll-snap-type: x mandatory;
}

.best-deal-slider::-webkit-scrollbar {
  /* display: none; */
}

.shop-category-wrap {
  display: grid;
  grid-auto-columns: 1fr;
  grid-column-gap: 23px;
  grid-row-gap: 16px;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
  grid-template-rows: auto;
}
.shop-category-area {
  padding-top: 80px;
  padding-bottom: 80px;
}

.categories-title,
.best-deal-title,
.brand-title {
  margin-top: 20px;
  margin-bottom: 40px;
  font-family: Eina02, sans-serif;
  font-size: 28px;
  line-height: 100%;
  font-weight: 700;
  text-transform: capitalize;
}
</style>
