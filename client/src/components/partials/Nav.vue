<template>
  <nav class="navbar is-danger" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    

    <a :class="{ 'is-active':isOpen }" @click="isOpen = !isOpen" role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div :class="{ 'is-active':isOpen }" class="navbar-menu">
    <div class="navbar-start">
      <router-link to="/" class="navbar-item" active-class="is-current">Home</router-link> 
      <router-link to="/about" class="navbar-item" active-class="is-current">About</router-link>
      <router-link to="/login" class="navbar-item" active-class="is-current">Login</router-link>
      
    </div>
  </div>
  
</nav>
</template>

<script>
export default {

data: ()=>({
  isOpen: false 
 })
}
</script>

<style lang="scss" scoped>
  nav {
    margin-top: 25px;
    margin-bottom: 30px;
    a {
      font-weight: bold;
      color: #2c3e50;
      &.router-link-exact-active {
        color:  #d45757;
      }
    }
  }
</style>