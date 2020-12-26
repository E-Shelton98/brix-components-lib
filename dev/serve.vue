<script>
import Vue from 'vue';
import { BrixComponentLibSample } from '@/entry';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    BrixComponentLibSample,
  }
});
</script>

<template>
  <div id="app">
    <brix-component-lib-sample />
  </div>
</template>
