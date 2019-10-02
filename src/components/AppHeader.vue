<template>
  <div class="header">
    <b-nav>
      <div class="center">
        <b-navbar-brand href="#">
          <img class="logo" alt="logo" src="../assets/logo.png" />
        </b-navbar-brand>
        <b-button variant="outline-primary btn-sm login">Login</b-button>
    
        <img @click="seen = !seen" class="cart" alt="Cart logo" src="../assets/cart.svg" />
        <div v-if="seen" class="cart-menu">
         <p>Item Item Item 1</p>
         <p>Item 1</p>
         <p>Item 1</p>
        </div>
      </div>
    </b-nav>
  </div>
</template>

<script>
export default {
  name: "AppHeader",
  data(){
  return {
    seen: false
  }
}
  
};
</script>

<style lang="scss">
.logo {
  width: 112px;
  margin-top: -8px;
}
.center {
  width: 800px;
  margin: 0 auto;
  display: flex;
  position: relative;
}
.header {
  margin-bottom: 30px;
}
.nav {
  padding: 10px;
  box-shadow: 1px 1px 3px #dedede;
  margin-bottom: 25px;
}

.cart {
  width: 30px;
  float: right;
  margin-top: -8px;
  position: absolute;
  right: 10px;
  top: 12px;
  cursor: pointer;
}
.login {
  position: absolute;
  right: 64px;
  top: 5px;
}
.cart-menu {
    position: absolute;
    right: -75px;
    background: #fff;
    top: 49px;
    padding: 21px;
    box-shadow: -1px 1px 3px #dcdcdc;
    z-index: 5;
}
</style>