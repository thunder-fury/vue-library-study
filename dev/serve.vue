<script lang="ts">
import Vue from 'vue';
// Uncomment import and local "components" registration if library is not registered globally.
import { VueLibrarySample } from '@/entry.esm';
import Cord from '../src/lib-components/vue-card.vue'
export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueLibrarySample,
    Cord
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
    <vue-library-sample />
    <Cord :onClick="(e) =>click(e)" label="button text" />
  </div>
</template>
