<template>
  <div class="container">
    <h1>Counter Game!</h1>
    <p>Clicks: {{ count }}<br><br>
        <button @click="onClick" @mouseover="hover = true" @mouseleave="hover = false" :class="{ active: hover }">Click me!</button>
    </p>
  </div>
</template>

<script>
export default {
  name: 'Counter',
  computed: {
    count() {
      return this.$store.state.count
    }
  },
  methods: {
    onClick() {
      this.$store.commit('increment')
    }
  }
}
</script>

<style scoped>
h1 {
  margin: 20px 0 0;
  font-size: 24px;
}
.container {
  border: 1px solid black;
  width: 600px;
  margin: 10px;
}
.active {
  background: #000000;
  color: #ffffff;
}
</style>