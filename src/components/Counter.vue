<template>
  <div>
    {{ count }}
    <button @click="increment">Plus</button>
    <button @click="decrement">Minus</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 1,
    }
  },
  methods: {
    increment: function () {
      this.count += 1
    },
    decrement: function () {
      this.count -= 1
    },
  },
}
</script>

<style scoped></style>
