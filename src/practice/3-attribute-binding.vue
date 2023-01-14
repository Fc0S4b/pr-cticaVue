<script>
export default {
  data() {
    return {
      message: 'Hello world',
      isRed: true,
      color: 'green'
    }
  },
  methods: {
    toggleRed() {
      this.isRed = !this.isRed
    },
    toggleColor() {
      this.color = this.color === 'green' ? 'blue' : 'green'
    }
  }
}
</script>

<template>
  <p>
    <span :title="message">
      Hello
    </span>
  </p>

  <p :class="{ red: isRed }" @click="toggleRed">
    hello 2
  </p>

  <p :style="{ color }" @click='toggleColor'>
    hello 3
  </p>

</template>


<style>
.red {
  color: red;
}
</style>