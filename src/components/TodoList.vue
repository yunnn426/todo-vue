<script setup>
    defineProps({
        tasks: Array,
    })
    
</script>

<template>
    <div class="todo-list">
        <h1 class="todo-title">---- Todo List ----</h1>
        <div class="todo" v-for="task in tasks">
            <input type="checkbox">
                <label for="checkbox">&nbsp;{{ task }}</label>
            </input>
        </div>
    </div>

</template>

<style scoped>
.todo-list {
    display: flex;
    flex-direction: column;
    align-items: center;

    background-image: url('../assets/paper.png');
    background-size : 444px 900px;
    background-position: center top;
    background-repeat: no-repeat;

    min-height: 1040px;
    padding: 20px;
    color: #606060;
}

.todo-title {
    font-family: 'watermelon';
    font-size: xxxx-large;
}

.todo {
    display: flex;
    padding: 10px;
    width: 250px;
}
</style>