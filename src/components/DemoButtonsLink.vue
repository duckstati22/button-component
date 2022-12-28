<script setup>
import BaseButton from "./UI/BaseButton.vue";
</script>
<template>
  <div class="demo-screen__column">
    <p class="column-header">(button link)</p>
    <div class="demo-screen__btn-group">
      <p class="btn-header">(hover)</p>
      <BaseButton class="link_custom-font" href="#" link>
        Напомнить PIN-код
      </BaseButton>
    </div>
    <div class="demo-screen__btn-group">
      <p class="btn-header">(pressed)</p>
      <BaseButton class="link_custom-font link_visited" href="#" link>
        Напомнить PIN-код
      </BaseButton>
    </div>
  </div>
</template>

<style scoped>
/* emulating visited */
.link_visited {
  color: #c4296c;
}
/* emulating visited */
.link_custom-font {
  font-family: "Nunito", sans-serif;
  font-size: 1rem;
  font-weight: bold;
  line-height: 1.125;
}
</style>
