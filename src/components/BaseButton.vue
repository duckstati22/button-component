<script setup>
import { computed } from "vue";

const props = defineProps({
  color: { type: String, default: "primary" },
  icon: Boolean,
  link: Boolean,
});

const buttonClassReducer = computed(() => {
  if (props.link) {
    return `base-link`;
  }
  if (props.icon) {
    return `base-btn base-btn_icon base-btn_${props.color}`;
  }
  return `base-btn base-btn_regular base-btn_${props.color}`;
});
</script>

<template>
  <a v-if="props.link" :class="buttonClassReducer">
    <slot></slot>
  </a>
  <button v-else :class="buttonClassReducer">
    <slot></slot>
  </button>
</template>

<style scoped>
button,
a {
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

.base-link {
  text-decoration: underline;
  text-decoration-skip-ink: none;
  transition: all 0.2s;
}
@media screen and (hover: hover) {
  .base-link:hover {
    color: var(--secondaryTextColor);
  }
}
.base-link:visited {
  color: var(--secondaryBackgroundColor);
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
.base-btn_icon {
  max-width: 60px;
  max-height: 60px;
  padding: 15px;
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
