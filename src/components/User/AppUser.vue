<template>
  <div class="component">
    <h3>Đây là bài test</h3>
    <p>Bài test về VueJs - Trao đổi thông tin giữa các Component - Author: {{ name }} - {{ age }}</p>
    <button class="btn btn-primary" @click="changeName">Chang Name</button>
    <hr>
    <div class="row">
      <div class="col-xs-12 col-sm-6">
        <UserDetail
            :customAge="age"
            :customName="name"
            @currentName="name = $event"
            :resetNameFn="resetName"
        />
      </div>
      <div class="col-xs-12 col-sm-6">
        <UserEdit
            :customName="name"
            :customAge="age"
            @currentAge="age = $event"
        />
      </div>
    </div>
  </div>
</template>

<script>
import UserDetail from "./UserDetail";
import UserEdit from "./UserEdit";

export default {
  data: function () {
    return {
      name: 'ChienNM',
      age: 18
    }
  },

  methods: {
    changeName: function () {
      this.name = 'Bun Real'
    },
    resetName: function () {
      this.name = 'ChienNM';
    }
  },

  components: {
    UserEdit,
    UserDetail
  }
}
</script>

<style scoped>
  div {
    background-color: lightblue;
  }
</style>
