<template>
    <div class="row">
        <todoItem class="todoItems" v-for="(item, index) in todoItems" @click.native="deleteItem(index)"> {{ item }}</todoItem>
    </div>
</template>

<script>
import TodoItem from './TodoItem.vue'

export default {
    props: ['todoItems'],
    components: {
        todoItem: TodoItem
    },
    methods: {
         deleteItem(index) {
            this.$emit('emitDelete')
        }
    }
}
</script>

<style>
    .todoItems {
        overflow-wrap: break-word;
    }
</style>

