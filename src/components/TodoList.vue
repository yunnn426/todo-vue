<script setup>
    import Todo from './Todo.vue'

    defineProps({
        tasks: Array,
    });

    // 오늘 날짜
    const today = new Date();
    const year = today.getFullYear();
    const month = today.getMonth() + 1;
    const date = today.getDate();
    const day = today.getDay();
    let strDay = '';
    switch (day) {
        case 1:
            strDay = 'Mon';
            break;
        
        case 2:
            strDay = 'Tue';
            break;

        case 3:
            strDay = 'Wed';
            break;

        case 4:
            strDay = 'Thu';
            break;
        
        case 5:
            strDay = 'Fri';
            break;

        case 6:
            strDay = 'Sat';
            break;
        
        case 7:
            strDay = 'Sun';
            break;

        default:
            break;
    }

    
</script>

<template>
    <div class="todo-list">
        <div class="todo-title">- - - - - - - Todo List - - - - - - -</div>
        <img src="../assets/cat.gif"/>
        <div class="todo-date">
            <div>Date: </div>
            <div class="str-date">&nbsp;{{ year }} / {{ month }} / {{ date }} ({{ strDay }})</div>
        </div>
        <div class="todo-header">
            <div>Tasks</div>
            <div class="check">Check</div>
        </div>
        <div class="todo-task">
            <div v-for="task in tasks" :key="task">
                <Todo :todo="task"/>
            </div>
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
    color: #606060;
}

.todo-title {
    font-family: 'watermelon';
    font-size: 32px;
    color: #806A5B;
    margin-top: 55px;
}

.todo-date {
    display: flex;

    font-family: 'watermelon';
    font-size: 28px;
    color: #806A5B;

    margin-top: 22px;
    width: 380px;
}

.str-date {
    color: #9C7559;
}

.todo-header {
    display: flex;
    justify-content: space-between;

    font-family: 'watermelon';
    font-size: 28px;
    color: #806A5B;

    width: 380px;
}

.check {
    margin-right: 30px;
}

.todo-task {
    margin-top: 30px;
}
</style>