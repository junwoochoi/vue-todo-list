<template>
    <div class="card">
        <div class="todo">{{this.todoItem.todo}}</div>
        <div class="hello" v-if="this.todoItem.state === 'active'">해야됨</div>
    </div>
</template>

<script>
export default {
    name: 'TodoItem',
    props: {
        todoItem: Object
    },
}
</script>

<style scoped>
.card{
    flex: 1;
    border: 1px solid #e9e9e9;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 2rem;
    margin: 0.25rem 1rem;
}

</style>

