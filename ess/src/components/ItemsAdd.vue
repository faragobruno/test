<template>
  <div class="items-look">
    <form @submit="addTodo">
         <input type="text" v-model="title" name="title" placeholder="Add items..">
         <input type="submit" value="Submit" class="btn">
     </form>
  </div>
</template>

<script>
export default {
  name: 'ItemsAdd',
  methods:{
        addItem(e){
            e.preventDefault();
            const newItem= {             
                title: this.title
            }
            this.$emit('add-item',newItem);
            this.title='';
        }
    }
}
</script>

<style scoped>
  .items-look{
    background:grey;
    color:black;
    border: 1px;
    width:520px;
    margin-left: 500px;
  }
  form{
        display: flex;
    }
    input[type="text"]{
        flex:10;
        padding: 2px;
    }
    input[type="Submit"]{
        flex:1;
    }
</style>
