<script>
// import Searchbar from './searchbar.vue'

// export default {
//   components: {
//     Searchbar
//   }
// }
</script>

<template>
  <section class="banner">
    <div class="container">
      <div class="banner-content">
        <div class="banner-content-title">
          <h1>Shopping And</h1>
          <h1>Department Store.</h1>
        </div>
        <div class="banner-content-paragraph">
          <p>
            Shopping is a bit of a relaxing hobby for me, which is sometimes troubling for the bank
            balance.
          </p>
        </div>
      </div>
      <div class="banner-button">
        <div class="button wrapper"><a class="button-text" href="#">Learn More</a></div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.container {
  max-width: 1360px;
  padding-left: 40px;
  padding-right: 40px;
  margin-right: auto;
  margin-left: auto;
}

.button-text {
  background-color: #003d29;
  border-radius: 50px;
  color: #ffffff;
  padding: 16px 36px;

  font-family: Eina02, sans-serif;
  font-size: 18px;
  line-height: 20px;
}
.banner-button {
  width: 100%;
  height: 100%;
}
.banner-content-paragraph {
  max-width: 495px;
  margin-bottom: 40px;
  color: #231f1e;
  font-size: 20px;
  line-height: 145%;
}
.banner-content-title {
  color: #003d29;
  text-transform: capitalize;
}

h1 {
  margin-top: 0px;
  font-family: Eina02, sans-serif;
  font-size: 64px;
  line-height: 74px;
  font-weight: 700;
  margin-bottom: 10px;
}
.banner {
  position: relative;
  width: 100%;
  z-index: 0;
  padding-top: 150px;
  padding-bottom: 150px;
  background-image: url('../assets/images/banner-bg.png');
  background-position: 50% 50%;
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
