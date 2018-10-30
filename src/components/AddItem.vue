<template>
    <div>
      <ul>
        <li v-for="todo,index in list" :key="index" class="todo-item">
          <span class="item-name">{{todo}}</span>

          <span @click="handDelete(index)" class="item-remove">X</span>
        </li>
      </ul>
    </div>
</template>

<script>
  export default {
    name: "Add",
    props:['list'],
    methods:{

      handDelete(index){
        this.list.splice(index,1)
      },

    }
  }

</script>

<style scoped lang='stylus'>
  ul
    list-style-position none
    padding 0
  .todo-item{
    padding: 16px 5px;
    border-bottom: 1px dashed #bbb;
    display: flex;
  }

  .todo-item:hover{
    background: #eee;
  }

  .item-name{
    flex-basis: 0;
    flex-grow: 9;
  }

  .item-remove{
    flex-basis: 0;
    flex-grow: 1;
    text-align: right;
    color: #EA1E63;
    font-weight: bold;
    cursor: pointer;
  }
</style>
