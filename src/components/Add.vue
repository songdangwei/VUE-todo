<template>

  <div class="wrapper">
    <input type="text" v-model="item"><button @click="handClick">添加</button>

  </div>

</template>

<script>
  export default {
    name: "Add",
    data() {
      return {
        item:'',
        list: []
      }
    },
      methods:{
      handClick(){

        if (this.item.trim() == '') return
        this.list.push(this.item)
        this.item = ''
        this.$emit("change", this.list)
      }
    }
  }

</script>

<style scoped lang='stylus'>
  .wrapper{
    display: flex;
  }
    input[type="text"]{
      flex-basis: 0;
      flex-grow: 7;
      flex: 1;
      padding: 10px;
      border: 2px solid #EA1E63;
      border-radius: 4px 0 0 4px;
      color: #777;
      outline: none;
    }

    button{
      padding: 10px;
      background: #EA1E63;
      border-radius: 0 4px 4px 0;
      border: 2px solid #EA1E63;
      color: #fff;
      text-transform: uppercase;
      cursor: pointer;
  }
</style>
