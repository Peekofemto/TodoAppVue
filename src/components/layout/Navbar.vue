<template>
<div>
  <b-navbar toggleable="lg" type="dark" variant="info">
    <h1 href="#">Todo List</h1>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="nav-links">
        <b-nav-item to="/">Home</b-nav-item>
        <b-nav-item to="/about" >About</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>

<script>
export default {
    name:"Navbar",
    data(){
      return{
        show: false
      }
    },
    methods: {
    }
}
</script>


<style scoped>
.nav-links li a{
    color: black;
    text-decoration: none;
    font-size: 16px;
  }
</style>