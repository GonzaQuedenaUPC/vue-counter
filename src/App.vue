<script setup>
  import {ref} from 'vue'

  let counter = ref(0);
  const reset = () => counter.value = 0;
  const increment = () => counter.value++;
  const decrement = () => counter.value--;
  const counterLimit = () => {
    if (counter.value < 0)
      return 'red';
    else if (counter.value > 0)
      return 'green';

    return '#000000';
  }
</script>

<template>
  <div class="container">
    <div class="counter">

      <h2 :style="{color: counterLimit()}" class="counter__label">
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
 

</style>
