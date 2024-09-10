<script setup>
import {computed, ref} from 'vue'

  let counter = ref(0);
  const reset = () => counter.value = 0;
  const increment = () => counter.value++;
  const decrement = () => counter.value--;

  const changeClassColor = computed(() => {
    if (counter.value < 0)
      return 'negative';

    if (counter.value > 0)
      return 'positive';

    return 'zero';
  })

</script>

<template>
  <div class="container">
    <div class="counter">

      <h2 :class="changeClassColor" class="counter__label">
        {{ counter }}
      </h2>

      <div class="counter__buttons">
        <button v-on:click="increment" class="counter__button counter__button--increment">Increment</button>
        <button v-on:click="reset" class="counter__button counter__button--reset">Reset</button>
        <button v-on:click="decrement" class="counter__button counter__button--decrement">Decrement</button>
      </div>

    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
.counter {
  box-shadow: 0 0 4px 10px rgba(0, 0, 0, 0.1);
  padding: 20px;
  border-radius: 1rem;
  text-align: center;
}

.counter__label {
  margin-bottom: 20px;
}

.counter__button {
  padding: 10px 20px;
  border: none;
  margin: 15px 10px 10px 10px;
  border-radius: 99999px;
  transition: .3s ease;
}

.counter__button--increment {
  box-shadow: 0 0 20px 0 #00ff00;
}
.counter__button--decrement {
  box-shadow: 0 0 20px 0 #ff0000;
}
.counter__button--reset {
  box-shadow: 0 0 20px 0 #0000ff;
}
.counter__button:hover {
  cursor: pointer;
  transform:translate(0, -5px);
}

.positive {
  color: #00ff00;
}
.negative {
  color: #ff0000;
}
.zero {
  color: #000000
}

</style>
