<template>
  <div class="dialog" v-if="show" @click="hideDialog">
    <div class="dialog__content">
      <h1>name</h1>
      <p>Lorem ipsum dolor sit amet.</p>
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
    border-radius: 12px;
    background: #fff;
    max-width: 510px;
    max-height: 516px;
    padding: 20px;
  }
}
</style>