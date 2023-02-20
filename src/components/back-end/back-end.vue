<template>
  <div class="back-end">
    <h2 style="margin: 80px 0 16px 0;">Бекенд разработчики</h2>
    <div class="back-content">
      <div 
        class="inner-content" 
        v-for="content in backContent" 
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
        backContent: [
          {id: 1, img: 'img', title: 'Исхокжон', body: 'Team Lead Backend'},
          {id: 2, img: 'img', title: 'Жавохир', body: 'Бекенд разработчик'},
          {id: 3, img: 'img', title: 'Сарвар ', body: 'Бекенд разработчик'},
          {id: 4, img: 'img', title: 'Шукурулло', body: 'Бекенд разработчик'},
          {id: 5, img: 'img', title: 'Жавохир', body: 'Бекенд разработчик'},
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
.back-end {
  margin-left: 92px;
  .back-content {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    padding: 10px;
    gap: 16px;
    width: 784px;
    height: 210px;
    background: #FAFAFA;
    border: 1px dashed #D5D8DF;
    border-radius: 28px;
    .inner-content {
      padding: 16px 12px;
      text-align: center;
      width: 140px;
      height: 188px;
      background: #FFFFFF;
      box-shadow: 0px 0px 4px rgba(0, 0, 0, 0.08), 0px 0px 2px rgba(0, 0, 0, 0.08);
      border-radius: 24px;
    }
  }
}
</style>