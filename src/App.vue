<script setup lang="ts">
import { RouterView, RouterLink } from 'vue-router'
</script>

<template>
  <div>
    <nav>
      <img src="@/assets/littlefean.jpg" alt="littlefean" class="icon" />
      <h2>我是标题</h2>
      <router-link to="">我是链接</router-link>
      <router-link to="">我是链接</router-link>
      <router-link to="">我是链接</router-link>
      <router-link to="">我是链接</router-link>
    </nav>
    <router-view></router-view>
  </div>
</template>

<style scoped lang="scss">
nav {
  background-color: rgba(59, 63, 65, 0.5);
  backdrop-filter: blur(5px);
  padding: 1em;
  margin: 1em;
  border-radius: 10px;
  display: flex;
  align-items: center;
  position: sticky;
  top: 1em;

  * {
    margin-right: 0.7em;
    height: 100%;
  }

  .icon {
    width: 2.5em;
    width: 2.5em;
    box-shadow: 0 0 20px #222;
    border-radius: 5px;
  }
}
</style>
