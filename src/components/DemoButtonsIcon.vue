<script setup>
import BaseButton from "./UI/BaseButton.vue";
</script>
<template>
  <div class="demo-screen__column">
    <p class="column-header">(button multi-sized)</p>
    <div class="demo-screen__btn-pair">
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">mobile</p>
        <BaseButton class="icon-btn_small" icon>
          <img draggable="false" src="../assets/icons/arrow-left.svg" alt="" />
        </BaseButton>
      </div>
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">desktop</p>
        <BaseButton icon>
          <img draggable="false" src="../assets/icons/arrow-left.svg" alt="" />
        </BaseButton>
      </div>
    </div>
    <div class="demo-screen__btn-pair">
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">mobile</p>
        <BaseButton class="icon-btn_small" icon color="danger">
          <img draggable="false" src="../assets/icons/exit.svg" alt="" />
        </BaseButton>
      </div>
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">desktop</p>
        <BaseButton icon color="danger">
          <img draggable="false" src="../assets/icons/exit.svg" alt="" />
        </BaseButton>
      </div>
    </div>
    <div class="demo-screen__btn-pair">
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">mobile</p>
        <BaseButton class="icon-btn_small icon-btn_custom-color" icon>
          <img draggable="false" src="../assets/icons/question.svg" alt="" />
        </BaseButton>
      </div>
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">desktop</p>
        <BaseButton class="icon-btn_custom-color" icon>
          <img draggable="false" src="../assets/icons/question.svg" alt="" />
        </BaseButton>
      </div>
    </div>
    <div class="demo-screen__btn-pair">
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">mobile</p>
        <BaseButton class="icon-btn_small" icon>
          <img draggable="false" src="../assets/icons/arrow-right.svg" alt="" />
        </BaseButton>
      </div>
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">desktop</p>
        <BaseButton icon>
          <img draggable="false" src="../assets/icons/arrow-right.svg" alt="" />
        </BaseButton>
      </div>
    </div>
    <div class="demo-screen__btn-pair">
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">mobile</p>
        <BaseButton class="icon-btn_small" icon color="danger">
          <img draggable="false" src="../assets/icons/google.svg" alt="" />
        </BaseButton>
      </div>
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">desktop</p>
        <BaseButton icon color="danger">
          <img draggable="false" src="../assets/icons/google.svg" alt="" />
        </BaseButton>
      </div>
    </div>
    <div class="demo-screen__btn-pair">
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">mobile</p>
        <BaseButton class="icon-btn_small" icon color="info">
          <img draggable="false" src="../assets/icons/vk.svg" alt="" />
        </BaseButton>
      </div>
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">desktop</p>
        <BaseButton icon color="info">
          <img draggable="false" src="../assets/icons/vk.svg" alt="" />
        </BaseButton>
      </div>
    </div>
    <div class="demo-screen__btn-pair">
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">mobile</p>
        <BaseButton class="icon-btn_small" icon color="action">
          <img draggable="false" src="../assets/icons/ok.svg" alt="" />
        </BaseButton>
      </div>
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">desktop</p>
        <BaseButton icon color="action">
          <img draggable="false" src="../assets/icons/ok.svg" alt="" />
        </BaseButton>
      </div>
    </div>
    <div class="demo-screen__btn-pair">
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">mobile</p>
        <BaseButton class="icon-btn_small" icon>
          <img draggable="false" src="../assets/icons/pen.svg" alt="" />
        </BaseButton>
      </div>
      <div class="demo-screen__btn-group">
        <p class="btn-header_lowercase">desktop</p>
        <BaseButton icon>
          <img draggable="false" src="../assets/icons/pen.svg" alt="" />
        </BaseButton>
      </div>
    </div>
  </div>
</template>

<style scoped>
.demo-screen__btn-pair {
  display: flex;
  column-gap: 24px;
}

/* emulating small buttons for mobile screens */
.icon-btn_small {
  max-width: 52px;
  max-height: 52px;
  padding: 14px;
}
.icon-btn_small > img {
  width: 24px;
  height: 24px;
}
/* emulating small buttons for mobile screens */

.icon-btn_custom-color {
  background-color: #6dd1b0;
}
</style>
