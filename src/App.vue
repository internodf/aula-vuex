<template>
  <div class="row">
    <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md6, col-md-offset-3">
      <h1>vuex</h1>
      <app-counter></app-counter>
      <app-result></app-result>
      <app-another></app-another>
    </div>
  </div>
</template>

<script>
  import Counter from './components/Counter.vue';
  import Result from './components/Result.vue';
  import AnotherResult from './components/AnotherResult.vue';

  export default {
    name: 'app',
    components: {
      appCounter: Counter,
      appResult: Result,
      appAnother: AnotherResult
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