<template>
  <div class="container">
    <h1>Counter Game!</h1>
    <p>Clicks: {{ counter }}<br><br>
        <button @click="counterClick" @mouseover="hover = true" @mouseleave="hover = false" :class="{ active: hover }">Click me!</button>
    </p>
  </div>
</template>

<script>
export default {
    data: function() {
        return {
            counter: 0,
            hover: false
        };
    },
    mounted() {
        const previousCounter = parseInt(localStorage.getItem("counter"));
        if (previousCounter != null) {
            this.counter = previousCounter
        }
    },
    methods: {
        counterClick: function(){
            this.counter += 1;
            localStorage.setItem("counter", this.counter);
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