<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
  export default {
    name: 'App',
    mounted() {
      /**
      * 解决 css 引入图片在 github pages 无法获取的问题
      */
//      const { NODE_ENV } = process.env;
//      document.documentElement.className = NODE_ENV;
    }
  }
</script>

<style lang="less">
//@import "~@/assets/global.less";
</style>
