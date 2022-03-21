<template>
  <div class="flex space-x-6 items-baseline">
    <button
        class="px-4 py-2 bg-emerald-100 border-2 border-emerald-300 rounded"
        @click="decreaseCounter">-
    </button>
    <span class="text 2xl font-semibold">{{ counter }}</span>
    <button
        class="px-4 py-2 bg-emerald-100 border-2 border-emerald-300 rounded"
        @click="increaseCounter">+
    </button>
  </div>
</template>

<!-- options api pattern-->
<script>
export default {
  data() {
    return {
      counter: 0
    }
  },
  methods: {
    increaseCounter() {
      this.counter++
    },
    decreaseCounter() {
      this.counter--
    }
  }
}
</script>
