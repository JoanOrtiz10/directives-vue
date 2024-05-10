<script setup>
import {ref} from 'vue' 

const users=["pepe", "Ana", "Juana","lola"]

const isChecked = ref(true)
</script>

<template>
    <ul>
        <li v-for="(user, index) in users" :key="index">{{index}}{{ user }}</li>
    </ul>
    <input type="checkbox" id="check" v-model="isChecked"/>
    <label for="check">pinchame</label>
    <div class="bg-blue-400 text-white rounded py-1 px-2  w-40 mx-auto" :class="{'bg-orange-500':isChecked}">
        Este es un mensaje 
    </div>
 <div v-show="isChecked">Hola </div>
 <div v-if="isChecked"> mundo</div>
 <div v-else>mateo es gay</div>





</template>