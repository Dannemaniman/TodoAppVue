<template>
    <div class="background">
        <div class="container">
            <myHeader :itemLength="items.length"> </myHeader>
            <newItem @addToList="addItem"></newItem>
            <todoGrid class="todo-grid" :todoItems="items" @emitDelete="deleteItem"></todoGrid>
        </div>        
    </div>
</template>

<script>
    import TodoGrid from './components/TodoGrid.vue'
    import NewItem from './components/NewItem.vue'
    import Header from './components/Header.vue'

    export default {
        data() {
            return {
                items: [],
            }
        },
        components: {
            todoGrid: TodoGrid,
            newItem: NewItem,
            myHeader: Header
        },
        methods: {
            addItem(itemToAdd) {
                this.items.push(itemToAdd.toUpperCase())
            },
            deleteItem(index) {
                this.items.splice(index, 1)
            }
        }
    }
</script>

<style>

    body {
        background-size: cover;
        background-position: center;
        background-attachment: fixed;
        transform: translate3d(0,0,0);
        -webkit-transform: translate3d(0,0,0);
        height: 100vh;
        background: linear-gradient(rgba(0, 0, 0, 1), rgba(0, 0, 0, 0.7)), url('./assets/headerpicture.jpg');
        background-color: black;
    }

    .todo-grid {
        margin-bottom: 10em;
    }

</style>
