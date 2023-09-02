<script>
import Searchbar from './searchbar.vue'

export default {
  components: {
    Searchbar
  }
}
</script>

<template>
  <div class="navbar">
    <div class="container">
      <div class="navbar-wrapper">
        <a href="#" class="navbar-brand"
          ><img alt="Vue logo" class="logo" src="../../assets/shopcart_logo.svg"
        /></a>
        <nav role="navigation" class="nav-menu">
          <ul>
            <li>
              <div class="nav-dropdown-wrapper">
                <div class="dropdown-text">Category</div>
                <div class="dropdown-icon"></div>
              </div>
            </li>
            <li><a href="#" class="nav-link">Deals</a></li>
            <li><a href="#" class="nav-link">What's New</a></li>
            <li><a href="#" class="nav-link">Delivery</a></li>
          </ul>
          <Searchbar />
        </nav>
        <div class="nav-right-content">
          <div class="nav-account-wrapper">
            <div class="account-icon"></div>
            <div class="account-text">Account</div>
          </div>
          <div class="nav-cart-wrapper">
            <div class="cart-icon"></div>
            <div class="cart-text">Cart</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.nav-account-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.nav-cart-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.account-icon {
  background-image: url('../../assets/user.png');
  background-repeat: no-repeat;
  height: 24px;
  width: 24px;
  margin-right: 11px;
}

.cart-icon {
  background-image: url('../../assets/cart.png');
  background-repeat: no-repeat;
  height: 24px;
  width: 24px;
  margin-right: 11px;
}
.nav-cart-wrapper {
  padding-left: 35px;
}
.nav-right-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.dropdown-icon {
  background-image: url('../../assets/dropdown.svg');
  background-repeat: no-repeat;
  height: 12px;
  width: 12px;
  margin-left: 8px;
}

.nav-dropdown-wrapper {
  display: flex;
  align-items: center;
  flex-wrap: nowrap;
}
.nav-link {
  margin-right: 5px;
  margin-left: 5px;
  padding: 5px 10px;
}
.nav-menu {
  /* background-color: aqua; */
  display: flex;

  align-items: center;

  justify-content: space-evenly;
}
.navbar-wrapper {
  vertical-align: middle;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  font-weight: 500;
}

.navbar {
  /* background-color: darkolivegreen; */

  /* font-size: 16px; */
  /* font-weight: 500; */
  line-height: 20px;
  color: #231f1e;

  margin: 0;
  padding: 15px;
  overflow: hidden;
  /* position: fixed; */
  top: 0;
  left: 0;
  /* width: 100%; */
  height: 52px;
}
li {
  display: inline-block;
  justify-content: space-between;
  padding: 5px 10px;
  /* background-color: gray; */
}
</style>
