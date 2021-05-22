<template>
  <div class="component">
    <h4>Edit the User here</h4>
    <p>Current Name: {{ customName }}</p>
    <p>My Age: {{ customAge }}</p>
    <button @click="changeAge">Change Age</button>
  </div>
</template>

<script>
import { eventBus } from '../../main.js';

export default {
  props: {
    customName: {
      type: String
    },
    customAge: {
      type: Number
    },
  },
  methods: {
    changeAge:  function () {
      this.customAge = 20;
      // this.$emit('currentAge', this.customAge)
      eventBus.$emit('ageWasEdit', this.customAge);
    }
  }

}
</script>

<style scoped>
    div {
      background: darkgoldenrod;
      height: 150px;
    }
</style>
