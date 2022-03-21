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

2 types of reactive data
refs : simple single items of data, eg a string, an array, a number
reactive objects : object of data with related data properties

don't need export default, setup() nor return statement
<!--composition api script setup pattern-->
<script setup>
import {ref} from "vue"

const counter = ref(0)

const increaseCounter = () => {
  counter.value++
}

const decreaseCounter = () => {
  counter.value--
}

</script>

<!--composition api setup function pattern-->
<!--<script>
import { ref } from "vue"

export default {
  setup() {
    const counter = ref(0)

    const increaseCounter = () => {
      counter.value++
    }

    const decreaseCounter = () => {
      counter.value--
    }

    return {
      counter,
      increaseCounter,
      decreaseCounter
    }
  }
}
</script>-->

<!-- options api pattern-->
<!--<script>
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
</script>-->
