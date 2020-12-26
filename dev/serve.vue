<script>
import Vue from 'vue';
import { BrixHeaderOne } from '@/entry';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    BrixHeaderOne,
  }
});
</script>

<template>
  <div id="app">
    <brix-header-one />
  </div>
</template>
