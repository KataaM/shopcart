<script setup>
import CategoryCard from './components/CategoryCard.vue'
import HeroBanner from './components/HeroBanner.vue'
import Navbar from './components/navbar/Navbar.vue'
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
  <!-- <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div> -->

  <!-- <main> 
    <TheWelcome />
  </main>  -->
</template>

<style scoped>
.container {
  max-width: 1280px;
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
.categories-title {
  margin-top: 20px;
  margin-bottom: 40px;
  font-family: Eina02, sans-serif;
  font-size: 28px;
  line-height: 100%;
  font-weight: 700;
  text-transform: capitalize;
}
/* header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
} */
</style>
