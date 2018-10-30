<template>
  <div class="row">
    <h4>another counter</h4>
    <button class="btn btn-primary" @click="increment(100)">Increment</button>
    <button class="btn btn-primary" @click="decrement(100)">Decrement</button>
  </div>
</template>

<script>
import { mapActions } from 'vuex';

export default {
  methods : {
      ...mapActions([
        'increment',
        'decrement',
        'asyncIncrement',
        'asyncDecrement'
      ]),
      // increment(by) {
      //   this.$store.dispatch('increment', by);
      // }
  }
}
</script>
