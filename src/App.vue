<template>
  <div class="row">
    <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md6, col-md-offset-3">
      <h1>vuex</h1>
      <app-counter></app-counter>
      <app-result></app-result>
      <app-another></app-another>
      <app-another-counter></app-another-counter>
      <hr/>
      <input type="text" -model="value" @input="updateValue">
      <p>{{ value }}</p>
    </div>
  </div>
</template>

<script>
  import Counter from './components/Counter.vue';
  import Result from './components/Result.vue';
  import AnotherResult from './components/AnotherResult.vue';
  import AnotherCounter from './components/AnotherCounter.vue';

  export default {
    name: 'app',
    components: {
      appCounter: Counter,
      appResult: Result,
      appAnother: AnotherResult,
      appAnotherCounter: AnotherCounter
    },
    computed: {
      value: {
        get() {
          return this.$store.getters.value;
        },
        set(value) {
          this.$store.dispatch('updateValue', event.target.value);
        }
      }
    },
    methods: {
      updateValue(event) {
        this.$store.dispatch('updateValue', event.target.value);
      }
    },
    data() {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    }
  }
</script>

<style>
</style>