<script setup>
import BaseButton from "./UI/BaseButton.vue";
</script>
<template>
  <div class="demo-screen__column">
    <p class="column-header">(button classic)</p>
    <div class="demo-screen__btn-group">
      <p class="btn-header">(primary)</p>
      <BaseButton>Отправить письмо</BaseButton>
    </div>
    <div class="demo-screen__btn-group">
      <p class="btn-header">(secondary)</p>
      <BaseButton color="secondary">Отправить письмо</BaseButton>
    </div>
    <div class="demo-screen__btn-group">
      <p class="btn-header">(warning)</p>
      <BaseButton color="warning">Отправить письмо</BaseButton>
    </div>
    <div class="demo-screen__btn-group">
      <p class="btn-header">(disabled)</p>
      <BaseButton disabled>Отправить письмо</BaseButton>
    </div>
    <div class="demo-screen__btn-group">
      <p class="btn-header">(info)</p>
      <BaseButton color="info">Отправить письмо</BaseButton>
    </div>
    <div class="demo-screen__btn-group">
      <p class="btn-header">(danger)</p>
      <BaseButton color="danger">Отправить письмо</BaseButton>
    </div>
    <div class="demo-screen__btn-group">
      <p class="btn-header">(action)</p>
      <BaseButton color="action">Отправить письмо</BaseButton>
    </div>
  </div>
</template>

<style scoped></style>
