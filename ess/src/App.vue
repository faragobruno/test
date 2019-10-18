<template>
  <div id="app">
    <Header />
    <ItemsAdd v-on:add-item="addItem"/>
    <ItemDatas v-bind:itemdatas="itemdatas" v-on:del-item="deleteItem"/>
    <Items />
  </div>
</template>

<script>
import ItemsAdd from './components/ItemsAdd.vue';
import Header from './components/layout/Header.vue';
import Items from './components/Items.vue';
import ItemDatas from './components/ItemDatas.vue';

export default {
  name: 'app',
  components:{
    ItemDatas,
    ItemsAdd,
    Header,
    Items
  },
  data(){
    return{
      itemdatas:[
        {
          id:1,
          title:"Adidas"
        },
        {
          id:2,
          title:"Nike"
        },
        {
          id:3,
          title:"Fila"
        },
        {
          id:4,
          title:"Vans"
        }
      ]
    }
  },
  methods:{
    deleteItem(id){
      this.itemdatas= this.itemdatas.filter(item => item.id != id)
    },
    addItem(newItem){
      this.itemdatas = [...this.itemdatas, newItem];
    }
  }
}
</script>

<style scoped>
</style>
