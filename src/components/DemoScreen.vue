<script setup>
import DemoButtonsLink from "./DemoButtonsLink.vue";
import DemoButtonsIcon from "./DemoButtonsIcon.vue";
import DemoButtonTimer from "./DemoButtonTimer.vue";
import DemoButtonsClassic from "./DemoButtonsClassic.vue";
</script>

<template>
  <div class="demo-screen">
    <DemoButtonsLink />
    <DemoButtonsIcon />
    <DemoButtonTimer />
    <DemoButtonsClassic />
  </div>
</template>

<style>
.demo-screen {
  max-width: 1548px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin: 50px auto 0;
  padding: 25px 38px;
  border: 8px solid #ffffff;
}

.demo-screen__column {
  display: flex;
  flex-direction: column;
  align-items: center;
  row-gap: 12px;
}
.demo-screen__btn-group {
  display: flex;
  flex-direction: column;
  row-gap: 8px;
}

@media screen and (max-width: 1140px) {
  .demo-screen {
    max-width: 715px;
    row-gap: 50px;
  }
  .demo-screen__column {
    width: 100%;
  }
}
</style>
