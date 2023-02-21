<template>
    <div 
      v-if="!contentVisible" 
      class="back-end" 
      @click="showDialog"
    >
      <h2 style="margin: 80px 0 16px 0;">BackEnd разработчики</h2>
      <div class="back-content">
        <div 
          class="inner-content" 
          v-for="content in backContent" 
          :key="content.id"
        >
          <img src="" alt="img">
          <h4 class="title">{{ content.title }}</h4>
          <p class="body">{{ content.body }}</p>
        </div>
      </div>
    </div>
    <!-- <my-dialog v-model:show="dialogVisible"></my-dialog> -->
    <div v-else>loading...</div>
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
          {id: 1, img: 'Исхокжон.png', title: 'Исхокжон', body: 'Team Lead Backend'},
          {id: 2, img: 'Жавохир.png', title: 'Жавохир', body: 'Бекенд разработчик'},
          {id: 3, img: 'Сарвар.png', title: 'Сарвар ', body: 'Бекенд разработчик'},
          {id: 4, img: 'Шукурулло.png', title: 'Шукурулло', body: 'Бекенд разработчик'},
          {id: 5, img: 'Жавохир2.png', title: 'Жавохир', body: 'Бекенд разработчик'},
        ],
        dialogVisible: false,
        contentVisible: false,
      }
    },
    methods: {
      showDialog() {
        this.dialogVisible = true;
      },
      loading() {
        setTimeout(() => {
          this.contentVisible = true;
        }, 2000)
      }
    }
  }
</script>

<style lang="scss" scoped>
.back-end {
  margin-left: 92px;
  position: relative;
  &::before {
    content: '';
    height: 2px;
    width: 50px;
    background-color: #fbc100;
    position: absolute;
  }
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
      cursor: pointer;
    }
  }
}
</style>