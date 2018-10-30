<template>
  <div class="wrapper">
    <router-link to="About">关于我</router-link>
    <h2>记事本</h2>
    <DoIssue :length="list.length"></DoIssue>
    <AddItem :list="list"></AddItem>
    <Add @change="addItem"></Add>
  </div>
</template>

<script>

  import Add from "./Add";
  import AddItem from './AddItem';
  import DoIssue from './DoIssue'


  export default {
    name: 'Home',
    data() {
      return {
        list: []
      }
    },
    methods: {
      addItem(list) {
        this.list = list
      },

    },
    components: {

      DoIssue,
      AddItem,
      Add
    }

  }
</script>

<style scoped lang='stylus'>



</style>
