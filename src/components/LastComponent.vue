<template>
  <div>
    <p>My Phone: {{ phone }}</p>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      phone: '909999999'
    }
  }
}
</script>

<style scoped>
  div {
    color: red;
  }
</style>
