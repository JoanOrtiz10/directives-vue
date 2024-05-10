<script setup>
import { ref } from 'vue'
const todos = ref(['Estudiar bastante'])
const todo = ref('')
function add() {
 console.log(todo);
    todos.value.unshift(todo.value)
    todo.value = ''

}

</script>
<template>
    <div class="  py-6 px-5  rounded shadow bg-slate-200 max-w-96 mx-auto mt-10">
        <div>
            <input v-model="todo" class="w-4/5 outline-none rounded px-2">
            <button @click="add" class=" w-1/5 bg-green-600 text-white text-center ">
                +

            </button>
        </div>
        <div class="mt-3">
            <div v-for="(todo, i) in todos" :key="i" class="px-1 rounded mt-4 bg-orange-300">
                {{ todo }}
            </div>

        </div>


    </div>
</template>