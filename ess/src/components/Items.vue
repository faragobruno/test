<template>
  <div class="items">
    <p>
    <button @click="$emit('del-item',item.id)" class="del">Törlés</button>
    {{item.title}}
    </p> 
  </div>
</template>

<script>
export default {
    name:'Items',
    props:["item"]
}
</script>

<style scoped>
    .items{
    background:bisque;
    color: black;
    border: 1px;
    width:520px;
    margin-left: 500px;
    }
    .del{
    display: inline-block;
    text-align: center;
    text-decoration: none;  
    margin: 2px 0;  
    border: solid 1px transparent;
    border-radius: 4px;  
    padding: 0.5em 1em;
    color: #ffffff;
    background-color: black;
    cursor: pointer;
}
</style>