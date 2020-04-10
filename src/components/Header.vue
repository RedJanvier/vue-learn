<template>
  <header>
      <div class="title">
      <h1>Robofriends</h1>
      </div>
      <div class="links">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
      </div>
  </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style>
    header {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        position: fixed;
        width: 100vw;
        top: 0;
        left: 0;
        border-bottom: 1px solid black;
        background: linear-gradient(45deg, rgb(37, 211, 211), rgb(30, 212, 112))
    }

    header h1 {
        text-align: center;
    }
</style>