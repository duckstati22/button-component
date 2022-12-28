<script setup>
import { ref, computed } from "vue";

const props = defineProps({
  timer: Number,
});

const timerMinutes = ref(0);
const formattedMinutes = computed(() => {
  if (timerMinutes.value < 10) {
    return `0${timerMinutes.value}`;
  }
  return timerMinutes.value;
});

const timerSeconds = ref(0);
const formattedSeconds = computed(() => {
  if (timerSeconds.value === 60) {
    return `00`;
  }
  if (timerSeconds.value < 10) {
    return `0${timerSeconds.value}`;
  }
  return timerSeconds.value;
});

function startTimer() {
  const endTime = Date.now() + props.timer;
  function timer() {
    const startTime = Date.now();
    const difference = endTime - startTime;
    timerMinutes.value = Math.floor(
      (difference % (1000 * 60 * 60)) / (1000 * 60)
    );
    timerSeconds.value = Math.ceil((difference % (1000 * 60)) / 1000);
    return timer;
  }
  const interval = setInterval(timer(), 1000);
  setTimeout(() => clearInterval(interval), props.timer);
}

// start timer when component created
startTimer();
</script>

<template>
  <div class="button-timer">
    {{ `${formattedMinutes}:${formattedSeconds}` }}
  </div>
</template>

<style scoped>
.button-timer {
  background-color: #df3f3e;
  color: #fff;
  border-radius: 11px 9px 11px 9px / 11px 12px 11px 12px;
  margin-left: 6px;
  padding: 1px 5.5px;
  width: 54px;
  height: 26px;
}
</style>
