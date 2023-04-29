<script setup lang="ts">
import { RouterView, RouterLink } from 'vue-router'

const totop = () => scrollTo(0, 0)
</script>

<template>
  <div>
    <nav>
      <span class="left" @click="totop" title="点我返回顶部">
        <img src="@/assets/littlefean.jpg" alt="littlefean" class="icon" />
        <h2>我是标题</h2>
      </span>
      <router-link to="/">首页</router-link>
      <router-link to="/history">history</router-link>
      <router-link to="/about">关于</router-link>
      <router-link to="/aaa">测试404页面</router-link>
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

  .left {
    flex: 1;
    display: flex;
    align-items: center;
  }
}
@media screen and (max-width: 600px) {
  nav {
    display: block;

    .left {
      margin-bottom: 0.5em;
    }
  }
}
@media screen and (max-width: 440px) {
  nav {
    a {
      display: block;
    }
  }
}
</style>
