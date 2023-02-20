<template>
  <div class="container">
    <h1 class="gl-title">Структрура IT подразделения Texnomart</h1>
    <div 
      class="content" 
      v-for="content in contents" 
      :key="content.id"
    >
      <img src="@/assets/ShuhratMengaliev.png" alt="img">
      <h4 class="title">{{ content.title }}</h4>
      <p class="body">{{ content.body }}</p>
    </div>
    <back-end />
    <front-end />
    <testing />
    <web-dizayn />
  </div>
</template>

<script>
import backEnd from './components/back-end/back-end.vue';
import frontEnd from './components/front-end/front-end.vue';
import testing from './components/testing/testing-it.vue';
import webDizayn from './components/web-dizayn/web-dizayn.vue';
export default {
  components: {
    backEnd, frontEnd, testing, webDizayn
  },
  data() {
    return {
      contents: [
        {id: 1, title: 'Шухрат Менгалиев', body: 'ИТ Директор'}
      ]
    }
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  padding: 80px 140px;
}
.container {
  max-width: 1400px;
  margin: 0 auto;
  .gl-title {
    font-style: normal;
    font-weight: 500;
    font-size: 40px;
    line-height: 140%;
    color: #333333;
    margin-bottom: 80px;
  }
  .content {
    border: 2px solid #fbc100;
    width: 210px;
    height: 198px;
    border-radius: 32px;
    padding: 24px 23px;
    text-align: center;
  }
}
.title {
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  line-height: 24px;
  color: #333333;
  margin: 20px 0 6px 0;
}
.body {
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #767676;
}
</style>
