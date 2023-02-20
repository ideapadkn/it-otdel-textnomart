<template>
  <div class="back-end" @click="showDialog">
    <h2 style="margin: 80px 0 16px 0;">BackEnd разработчики</h2>
    <div class="back-content">
      <div 
        class="inner-content" 
        v-for="content in backContent" 
        :key="content.id"
      >
        <my-dialog v-model:show="dialogVisible">
          <img :src="content.img" alt="img">
        </my-dialog>
        <h4 class="title">{{ content.title }}</h4>
        <p class="body">{{ content.body }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import myDialog from './my-dialog.vue';
  export default {
    components: {
      myDialog
    },
    data() {
      return {
        backContent: [
          {id: 1, img: '@/assets/back-end/Исхокжон.png', title: 'Исхокжон', body: 'Team Lead Backend'},
          {id: 2, img: '@/assets/back-end/Жавохир.png', title: 'Жавохир', body: 'Бекенд разработчик'},
          {id: 3, img: '@/assets/back-end/Сарвар.png', title: 'Сарвар ', body: 'Бекенд разработчик'},
          {id: 4, img: '@/assets/back-end/Шукурулло.png', title: 'Шукурулло', body: 'Бекенд разработчик'},
          {id: 5, img: '@/assets/back-end/Жавохир2.png', title: 'Жавохир', body: 'Бекенд разработчик'},
        ],
        dialogVisible: false,
      }
    },
    methods: {
      showDialog() {
        this.dialogVisible = true;
      }
    }
  }
</script>

<style lang="scss" scoped>
.back-end {
  margin-left: 92px;
  .back-content {
    display: inline-flex;
    flex-direction: row;
    align-items: flex-start;
    padding: 10px;
    gap: 16px;
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