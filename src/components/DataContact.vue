<template>
  <div>
    <p>My Address: {{ address }}</p>
    <hr>
<!--    <button :class="btnPrimary" @click="changeAddress()">Show</button>-->
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      address: 'Nam Định',
      btnPrimary: 'btn btn-primary'
    }
  },
  methods: {
    changeAddress: function () {
      this.address = 'Hà Noi';
    }
  }
}
</script>

<style lang="scss" scoped>
    div {
      color: blue;
    }
</style>
