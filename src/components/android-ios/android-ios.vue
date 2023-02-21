<template>
  <div class="mobile">
    <h2 style="margin: 80px 0 16px 0;">Разработка приложений Android/iOS </h2>
    <div class="mobile-content">
      <div 
        class="inner-content" 
        v-for="content in webUiUxContent" 
        :key="content.id"
      >
        <div>{{ content.img }}</div>
        <h4 class="title">{{ content.title }}</h4>
        <p class="body">{{ content.body }}</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        webUiUxContent: [
          {id: 1, img: 'img', title: 'Муроджон', body: 'Team Lead Android/iOS'},
          {id: 2, img: 'img', title: 'Зухриддин', body: 'Android/iOS'},
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
.mobile {
  margin-left: 100px;
  position: relative;
  .mobile-content {
    display: inline-flex;
    flex-direction: row;
    align-items: flex-start;
    padding: 10px;
    gap: 16px;
    height: 210px;
    background: #FAFAFA;
    border: 1px dashed #D5D8DF;
    border-radius: 28px;
    &::before {
      content: '';
      height: 2px;
      width: 50px;
      background-color: #fbc100;
      position: absolute;
      left: -6%;
      top: 50%;
    }
    .inner-content {
      padding: 16px 12px;
      text-align: center;
      width: 140px;
      height: 188px;
      background: #FFFFFF;
      box-shadow: 0px 0px 4px rgba(0, 0, 0, 0.08), 0px 0px 2px rgba(0, 0, 0, 0.08);
      border-radius: 24px;
      cursor: pointer;
    }
  }
}
</style>