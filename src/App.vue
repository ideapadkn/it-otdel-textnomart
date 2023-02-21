<template>
  <div class="container">
    <h1 class="gl-title">Структрура IT подразделения Texnomart</h1>
    <div class="main-wrapper">
      <div 
        class="content" 
        v-for="content in contents" 
        :key="content.id"
      >
        <img src="@/assets/ShuhratMengaliev.png" alt="img">
        <h4 class="title">{{ content.title }}</h4>
        <p class="body">{{ content.body }}</p>
      </div>
    </div>
    <div class="sortByWork">
      <div 
        class="sort" 
        v-for="sort in sortWork" 
        :key="sort.id"
      >
        <h4 class="sort__title">{{ sort.text }}</h4>
      </div>
    </div>
    <back-end />
    <front-end />
    <testing />
    <web-dizayn />
    <android-ios />
    <dev-ops />
  </div>
</template>

<script>
import backEnd from './components/back-end/back-end.vue';
import frontEnd from './components/front-end/front-end.vue';
import testing from './components/testing/testing-it.vue';
import webDizayn from './components/web-dizayn/web-dizayn.vue';
import androidIos from './components/android-ios/android-ios.vue';
import devOps from './components/dev-ops/dev-ops.vue';
export default {
  components: {
    backEnd, frontEnd, testing, webDizayn, androidIos, devOps
  },
  data() {
    return {
      contents: [
        {id: 1, title: 'Шухрат Менгалиев', body: 'ИТ Директор'}
      ],
      sortWork: [
        {id: Date.now(), text: 'Разработка ПО'},
        {id: Date.now(), text: 'Системные инженеры'},
        {id: Date.now(), text: 'Ремонт и переферия'},
        {id: Date.now(), text: 'Электро монтаж'},
      ],
      dialogVisible: false,
    }
  },
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
  .main-wrapper {
    position: relative;
    .content {
      border: 2px solid #fbc100;
      width: 210px;
      height: 198px;
      border-radius: 32px;
      padding: 24px 23px;
      text-align: center;
      &::before {
        content:'';   
        top: 50%;
        left: 210px;
        height: 2px;
        position: absolute;
        width: 78%;
        background:#fbc100;
        border-bottom-right-radius: 30px;
      }
    }
  }
  .sortByWork {
    display: flex;
    justify-content: space-between;
    margin-left: 309px;
    margin-bottom: 200px;
    position: relative;
    .sort {
      border: 2px solid #333333;
      border-radius: 16px;
      padding: 12px 24px;
      &::before {
        content: '';
        height: 2px;
        width: 50px;
        background-color: #fbc100;
        position: absolute;
        top: -30%;
        left: 6%;
      }
      &__title {
        font-style: normal;
        font-weight: 500;
        font-size: 18px;
        line-height: 24px;
        text-align: center;
        color: #333333;
      }
    }
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
