<template>
<div class="input-wrapper">
    <h2>TODO</h2>
    <input type="text" v-model="todoItem"/>
    <button @click="createTodo">완료</button>
</div>
</template>

<script>
export default {
    name: "TodoInput",
    data(){
        return{
            todoItem: null
        }
    },
    methods:{
        createTodo: function(){
            const todoItem = {
                todo: this.todoItem,
                state: 'active'
            };
            
            this.$emit("createTodo", todoItem);
            
            this.todoItem = null;

        }
    }
}
</script>

<style scoped>
.input-wrapper{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
input{
    margin: 0.25rem 1rem;
    min-width: 15rem;
    padding: 0.25rem;
}
button{
    padding: 0.25rem 0.5rem;
    border: 1px solid #efefef;
    border-radius: 0.25rem;
}

button:active{
    
}
</style>

