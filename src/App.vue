<template>
  <div id="app">
    <img src="./assets/logo.png">
    <van-loading color="black" />
      <van-loading color="white" />
      <van-loading type="spinner" color="black" />
      <van-loading type="spinner" color="white" />
      <van-rate v-model="value" />
      <van-nav-bar
  title="标题"
  left-text="返回"
  
  left-arrow
  @click-left="onClickLeft"
  @click-right="onClickRight"
/>
    <router-view/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: 3
    };
  },
  methods: {
    onClickLeft() {
      Toast('返回');
    },
    onClickRight() {
      Toast('');
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
