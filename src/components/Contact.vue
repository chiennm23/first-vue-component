<template>
  <div>
    <h2>From Contact Component</h2>
    <DataContact/>
    <LastComponent/>
  </div>
</template>
<script>
import DataContact from "./DataContact";
import LastComponent from "./LastComponent";

export default {
  components: {
    LastComponent,
    DataContact
  }
}
</script>

<style lang="scss" scoped>
  div {
    color: black;
  }
</style>
