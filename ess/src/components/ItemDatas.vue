<template>
    <div>
        <div v-bind:key="item.id" v-for="item in itemdatas" >
            <Items v-bind:item="item" v-on:del-item="$emit('del-item',item.id)" />
        </div>
    </div>
</template>

<script>
import Items from './Items.vue';
export default {
    name: 'ItemDatas',
    components:{
        Items
    },
    props:["itemdatas"]
}
</script>

<style>

</style>