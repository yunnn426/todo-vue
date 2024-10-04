<script setup>
    defineProps({
        todo: String,
    })
</script>

<template>
    <div class="todo">
        <label :for="todo">{{ todo }}</label>
        <input class="check" type="checkbox" :id="todo"/>
    </div>
</template>

<style scoped>
.todo {
    display: flex;
    justify-content: space-between;

    font-family: 'watermelon';
    font-size: 24px;
    color: #9C7559;
    
    padding: 5px;
    width: 380px;
}

.check {
    margin-right: 35px;
}
</style>