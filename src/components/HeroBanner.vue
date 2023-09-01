<script></script>

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
    <div class="banner-stage-wrap">
      <div class="banner-stage-bg">
        <img src="../assets/images/banner-yellow-stairs.png" alt="" />
      </div>
      <div class="product-image-one">
        <img src="../assets/images/product-image-1.png" alt="" />
      </div>
      <div class="product-image-two">
        <img src="../assets/images/product-image-2.png" alt="" />
      </div>
      <div class="product-image-three">
        <img src="../assets/images/product-image-3.png" alt="" />
      </div>
      <div class="product-image-four">
        <img src="../assets/images/product-image-4.png" alt="" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.product-image-two {
  position: absolute;
  left: auto;
  top: 156px;
  right: 433px;
  bottom: auto;
}
.product-image-three {
  position: absolute;
  left: auto;
  top: 300px;
  right: 208px;
  bottom: auto;
}
.product-image-four {
  position: absolute;
  left: auto;
  top: 350px;
  right: 550px;
  bottom: auto;
}
.product-image-one {
  position: absolute;
  left: auto;
  top: 71px;
  right: 125px;
  bottom: auto;
}
.banner-stage-bg {
  text-align: right;
}
img {
  max-width: 100%;
  vertical-align: middle;
  display: inline-block;
  text-align: right;
}
.banner-stage-wrap {
  position: absolute;
  top: 0%;
  left: 0%;
  right: auto;
  bottom: auto;
  z-index: -1;
  width: 100%;
  height: 100%;
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
  padding-top: 16px;
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
  margin-bottom: 30px;
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
  padding-bottom: 180px;
  background-image: url('../assets/images/banner-bg.png');
  background-position: 50% 50%;
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
