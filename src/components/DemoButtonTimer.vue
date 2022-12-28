<script setup>
import BaseButton from "./UI/BaseButton.vue";
</script>
<template>
  <div class="demo-screen__column timer-buttons__column">
    <p class="column-header">(button timer)</p>
    <div class="demo-screen__btn-group">
      <p class="btn-header">(timer, click to show)</p>
      <BaseButton
        timer="180"
        replacement-text="повторное письмо"
        color="action"
      >
        Отправить письмо
      </BaseButton>
    </div>
  </div>
</template>

<style scoped>
.timer-buttons__column {
  flex-basis: 297px;
}
@media screen and (max-width: 1140px) {
  .timer-buttons__column {
    flex-basis: auto;
  }
}
</style>
