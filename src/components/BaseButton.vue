<script setup>
import { computed } from "vue";

const props = defineProps({
  color: { type: String, default: "primary" },
});

const buttonClassReducer = computed(() => {
  return `base-btn base-btn_regular base-btn_${props.color}`;
});
</script>

<template>
  <button :class="buttonClassReducer">
    <slot></slot>
  </button>
</template>

<style scoped>
button {
  --primaryBackgroundColor: #702c7e;
  --secondaryBackgroundColor: #c4296c;
  --warningBackgroundColor: #f4ba46;
  --disabledBackgroundColor: #efefef;
  --infoBackgroundColor: #0083b6;
  --dangerBackgroundColor: #df3f3e;
  --actionBackgroundColor: #ed732e;
  --primaryTextColor: #fff;
  --secondaryTextColor: #767679;

  all: unset;
  display: revert;
  box-sizing: border-box;
  cursor: pointer;
}

.base-btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 20px 20px 20px 20px / 21px 20px 21px 20px;
  color: var(--primaryTextColor);
  text-transform: uppercase;
  transition: all 0.2s;
}
.base-btn:disabled {
  background-color: var(--disabledBackgroundColor);
  color: var(--secondaryTextColor);
  cursor: auto;
}
@media screen and (hover: hover) {
  .base-btn:hover {
    filter: opacity(0.5);
  }
  .base-btn:active,
  .base-btn:disabled {
    filter: opacity(1);
  }
}

.base-btn_regular {
  padding: 0.78em 1.75em;
}

.base-btn_primary {
  background-color: var(--primaryBackgroundColor);
}
.base-btn_secondary {
  background-color: var(--secondaryBackgroundColor);
}
.base-btn_warning {
  background-color: var(--warningBackgroundColor);
}
.base-btn_info {
  background-color: var(--infoBackgroundColor);
}
.base-btn_danger {
  background-color: var(--dangerBackgroundColor);
}
.base-btn_action {
  background-color: var(--actionBackgroundColor);
}
</style>
