
<template>

  <div>

     <p v-if="length<=0">所有事情都已完成</p>

    <p v-if="length>0">明日复明日,明日何其多</p>

  </div>
</template>


<script>

    export default {
        name: "DoIssue",
        props:['length']
    }
</script>

<style scoped lang='stylus'>
   p
     color: #777;
     font-style: italic;
</style>
