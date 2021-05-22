<template>
  <div class="component">
    <h4>Infomation User Detail</h4>
    <p>List Detail</p>
    <p>My Name: {{ customName }} - {{ customAge }}</p>
    <button @click="resetName">Reset Name</button>
    <button @click="resetNameFn">Name Callback</button>
  </div>
</template>

<script>
import { eventBus } from '../../main.js';

export default {
  props: {
    customName: {
      type: String,
      required: true
    },
    customAge: {
      type: Number
    },
    resetNameFn: Function,
  },
  methods: {
    resetName: function () {
      this.customName = "ChienNM";
      this.$emit('currentName', this.customName);
    }
  },

  created() {
    eventBus.$on('ageWasEdit', (age) => {
      this.customAge = age;
    })
  }
}
</script>

<style scoped>
div {
  background: rosybrown;
  height: 150px;
}
</style>
