<script lang="ts">
import Vue from 'vue';
// Uncomment import and local "components" registration if library is not registered globally.
import { Card } from '@thunder_fury/vue-library'
export default Vue.extend({
  name: 'ServeDev',
  components: {
    Card
  },
  methods: {
    click(e: Event) {
      console.log(e.target)
    }
  }
});
</script>

<template>
  <div id="app">
    <Card label="adsfasdfdddddddddddd" />
  </div>
</template>
