<template>
  <div class="dialog" v-if="show" @click.stop="hideDialog">
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
        <div class="content__inner-item">
          <div>
            <p class="info__text">Работает с нами</p>
            <h3>1 год 5 месяцев</h3>
          </div>
          <div>
            <p class="info__text">ЗП</p>
            <h3>** *** *** сум</h3>
          </div>
        </div>
        <div>
          <p class="info__text">Участвовал в проекте</p>
          <a target="_blank" class="link" href="#">Texnomart Web Design</a>
          <a target="_blank" class="link" href="#">Android App</a>
        </div>
        <div>
          <p class="info__text">Интересы</p>
          <span class="span">Теннис</span>
          <span class="span">CS:GO</span>
          <span class="span">Кино</span>
          <span class="span">Путешествия</span>
        </div>
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
      &:nth-child(3) {
        flex-direction: column;
      }
      .block {
        border-right: 1px dashed #D5D8DF;
        padding-right: 60px;
        &:nth-child(3) {
          border: none;
        }
      }
      .content__inner-item {
        display: flex;
        justify-content: space-between;
      }
      .link {
        font-style: normal;
        font-weight: 400;
        font-size: 11px;
        line-height: 16px;
        color: #333333;
        padding: 4px 8px;
        background: #EEEEEE;
        border-radius: 50px;
        text-decoration: none;
        margin-right: 6px;
      }
      .span {
        font-style: normal;
        font-weight: 400;
        font-size: 11px;
        line-height: 16px;
        color: #333333;
        border: 1px solid #D5D8DF;
        margin-right: 10px;
        padding: 3px 6px;
        border-radius: 30px;
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