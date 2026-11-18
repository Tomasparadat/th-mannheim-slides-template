<script setup lang="ts">
import { ref } from 'vue'

withDefaults(defineProps<{ label?: string }>(), { label: 'Zähler' })
const count = ref(0)
</script>

<template>
  <div class="counter-demo">
    <span>{{ label }}</span>
    <div class="counter-value" aria-live="polite" aria-atomic="true">
      <Transition name="counter" mode="out-in">
        <strong :key="count">{{ count }}</strong>
      </Transition>
    </div>
    <div class="counter-actions">
      <button type="button" @click.stop="count++">+1</button>
      <button type="button" @click.stop="count = 0">Zurücksetzen</button>
    </div>
  </div>
</template>

<style scoped>
.counter-demo {
  padding: 24px;
  border: 2px solid var(--th-blue);
  border-radius: 12px;
  text-align: center;
  line-height: 1.4;
}
.counter-value {
  height: 72px;
  font-size: 48px;
  color: var(--th-blue);
}
.counter-value strong { display: inline-block; }
.counter-actions { display: flex; justify-content: center; gap: 16px; }
button {
  padding: 8px 18px;
  border: 1px solid var(--th-blue);
  border-radius: 6px;
  background: var(--th-light);
  color: var(--th-blue);
  font: inherit;
  cursor: pointer;
}
button:hover { background: var(--th-blue); color: var(--th-white); }
button:focus-visible { outline: 3px solid var(--th-blue); outline-offset: 3px; }
.counter-enter-active, .counter-leave-active { transition: opacity .15s, transform .15s; }
.counter-enter-from { opacity: 0; transform: translateY(12px); }
.counter-leave-to { opacity: 0; transform: translateY(-12px); }
@media (prefers-reduced-motion: reduce) {
  .counter-enter-active, .counter-leave-active { transition: none; }
}
</style>
