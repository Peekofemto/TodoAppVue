<template>
  <nav>
    <div @click="show=!show" class="hamburger">
      <div class="line"></div>
      <div class="line"></div>
      <div class="line"></div>
    </div>
    <transition>
    <ul v-if="show" class="nav-links">
      <li>
        <h1>TodoList</h1>
      </li>
      <li>
        <router-link to="/">Home</router-link>
      </li>
      <li>
        <router-link to="/about">About</router-link>
      </li>
    </ul>
    </transition>
  </nav>
</template>

<script>
export default {
    name:"Header",
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
  .v-enter-active{
    animation: bounceOff 2s;
  }

  .v-leave-active{
    animation: bounceOff 2s reverse;
  }

  @keyframes bounceOff {
    0%{
      position: fixed;
      background: #5b78c7;
      height: 100vh;
      width: 100%;
      flex-direction: column;
      clip-path: circle(100px at 90% 10%);
      -webkit-clip-path: circle(100px at 90% 10%);
      transition: all 1s ease-out;
    }
    100%{
    clip-path: circle(1000px at 90% 10%);
    -webkit-clip-path: circle(1000px at 90% 10%);
    }
  }

  nav{
    font-family: sans-serif;
    height: 10vh;
    background: #5b68c7;
  }
  .nav-links{
    display: flex;
    list-style: none;
    width: 50%;
    height: 100%;
    justify-content: space-around;
    align-items: center;
    margin-left: auto;
  }
  .nav-links li a{
    color: white;
    text-decoration: none;
    font-size: 16px;
  }

  @media screen and (max-width: 768px){
  .line{
    width: 30px;
    height: 3px;
    background: white;
    margin: 5px;
  }

  nav{
    position: relative;
  }

  .hamburger{
    position: absolute;
    cursor: pointer;
    right: 5%;
    top: 50%;
    transform: translate(-5%, -50%);
    z-index: 2;
  }

  .nav-links{
    
  }
  .nav-links.open{
    
  }
  }

</style>