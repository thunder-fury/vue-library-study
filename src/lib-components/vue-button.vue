<template>
  <div>
    <button
      value="buttonVal"
      :style="style"
      @click="onClick">
      {{ label }}
    </button>
    <!-- <input @:change="(e)=>inputEvent" type="text"> -->
  </div>
</template>
<script lang="ts">
import Vue from 'vue';

interface SampleData {
  toggle: boolean
  te: string
}

export default Vue.extend({
  name: 'VueLibrarySample', // vue component name
  props: {
    label: String,
    backgroundColor: String,
    onClick: Function,
  },
  data(): SampleData {
    return {
      toggle: false,
      te: '',
    };
  },
  mounted() {
    console.log()

  },
  computed: {
    style() {
      return {
        backgroundColor: this.backgroundColor
      }
    }
  },
  methods: {
    eventFun(_e: Event) {
      console.log(_e.target)
    },
  },
});
</script>

<style scoped>
  .vue-library-sample {
    display: block;
    width: 400px;
    margin: 25px auto;
    border: 1px solid #ccc;
    background: #eaeaea;
    text-align: center;
    padding: 25px;
  }
  .vue-library-sample p {
    margin: 0 0 1em;
  }
</style>
