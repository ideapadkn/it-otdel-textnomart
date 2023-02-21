<template>
  <div class="dialog" v-if="show" @click="hideDialog">
    <div class="dialog__content">
      <div class="content__inner">
        <div class="img">
          <img width="120px" height="120px" src="@/assets/back-end/Исхокжон.png" alt="img">
        </div>
        <div class="info">
          <p class="info__text">ФИО</p>
          <h3 class="info__title">Ахмедов Исхокжон Иброхимжон огли</h3>
          <p class="info__text">Дата рождения</p>
          <p class="info__text">05.04.1997 г</p>
        </div>
      </div>
      <div class="content__inner">
        <div class="block">
          <p class="info__text">
            Должность
          </p>
          <h3 class="info__title">Backend</h3>
        </div>
        <div class="block">
          <p class="info__text">
            Уровень
          </p>
          <h3 class="info__title">Senior</h3>
        </div>
        <div class="block">
          <p class="info__text">
            Опыт
          </p>
          <h3 class="info__title">5 лет</h3>
        </div>
      </div>
      <div class="content__inner">
        
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      show: {
        type: Boolean,
        default: false
      }
    },
    methods: {
      hideDialog() {
        this.$emit('update:show', false)
      }
    }
  }
</script>

<style lang="scss" scoped>
.dialog {
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba($color: #b7b7b7ca, $alpha: 0.3);
  position: fixed;
  display: flex;
  &__content {
    margin: auto;
    border-radius: 24px;
    box-shadow: 0px 2px 16px 1px rgba(0, 0, 0, 0.04);
    background: #fff;
    max-width: 510px;
    max-height: 516px;
    padding: 20px;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    .content__inner {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      margin-bottom: 20px;
      padding: 10px;
      &:nth-child(2) {
        border-top: 1px dashed #D5D8DF;
        border-bottom: 1px dashed #D5D8DF;
      }
      .block {
        border-right: 1px dashed #D5D8DF;
        padding-right: 60px;
        &:nth-child(3) {
          border: none;
        }
      }
      .info {
        &__title {
          font-style: normal;
          font-weight: 700;
          font-size: 16px;
          line-height: 24px;
          letter-spacing: 0.2px;
          color: #333333;
        }
        &__text {
          font-style: normal;
          font-weight: 400;
          font-size: 13px;
          line-height: 18px;
          color: #767676;
          margin-bottom: 6px;
        }
      }
    }
  }
}
</style>