<template>
    <header>
      <nav>
        <router-link to="/" class="menu">Home</router-link>
        <router-link to="/contact" class="menu">Contact Me</router-link>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    name: 'Header',
  };
  </script>
  
  <style scoped>

  .menu {
    color: rgb(255, 255, 255);
  }
  
  header {
    background-color: #333;
    color: white;
    padding: 10px;
    margin-bottom: 10%;
    
  }
  
  nav {
    display: flex;
    justify-content: space-around;
  }
  
  router-link {
    text-decoration: none;
    color: white;
    font-weight: bold;
  }
  </style>
  