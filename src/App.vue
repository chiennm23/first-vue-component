<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <AppUser/>
      </div>
    </div>

  </div>
</template>

<script>
// import Contact from "./components/Contact";
import AppUser from "./components/User/AppUser";


export default {
  components: {
    AppUser
  }
}
</script>

<style lang="scss" scoped>
    div.component {
      border: 1px solid black;
      padding: 30px;
    }
</style>
