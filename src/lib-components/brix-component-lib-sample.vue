<script>
export default {
  name: 'BrixComponentLibSample', // vue component name
  data() {
    return {
      counter: 5,
      initCounter: 5,
      message: {
        action: null,
        amount: null,
      },
    };
  },
  computed: {
    changedBy() {
      const { message } = this;
      if (!message.action) return 'initialized';
      return `${message?.action} ${message.amount ?? ''}`.trim();
    },
  },
  methods: {
    increment(arg) {
      const amount = (typeof arg !== 'number') ? 1 : arg;
      this.counter += amount;
      this.message.action = 'incremented by';
      this.message.amount = amount;
    },
    decrement(arg) {
      const amount = (typeof arg !== 'number') ? 1 : arg;
      this.counter -= amount;
      this.message.action = 'decremented by';
      this.message.amount = amount;
    },
    reset() {
      this.counter = this.initCounter;
      this.message.action = 'reset';
      this.message.amount = null;
    },
  },
};
</script>

<template>
  <div class="brix-component-lib-sample">
    <p>The counter was {{ changedBy }} to <b>{{ counter }}</b>.</p>
    <button @click="increment">
      Click +1
    </button>
    <button @click="decrement">
      Click -1
    </button>
    <button @click="increment(5)">
      Click +5
    </button>
    <button @click="decrement(5)">
      Click -5
    </button>
    <button @click="reset">
      Reset
    </button>
  </div>
</template>

<style scoped lang="scss">
  .brix-component-lib-sample {
    display: block;
    width: 400px;
    margin: 25px auto;
    border: 1px solid #ccc;
    background: lightgray;
    text-align: center;
    padding: 25px;
  }
  .brix-component-lib-sample p {
    margin: 0 0 1em;
  }
</style>
