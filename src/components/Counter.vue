<script setup lang="ts">
const props = defineProps<{
  initial: number
}>()
defineEmits<{
  (event: 'test', count: string): void
}>()

const { count, inc, dec } = useCounter(props.initial)
</script>

<template>
  <div>
    {{ count }}
    <button class="inc" @click="inc()">
      +
    </button>
    <button class="dec" @click="dec()">
      -
    </button>
  </div>
</template>
