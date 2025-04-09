<template>
    <div>
        <h2>Lista de tareas</h2>
        <input type="text" v-model="nuevaTarea" placeholder="escribe las tareas" @keyup.enter="addTarea">
        <ul>
            <li v-for="(tarea, index) in tareas" :key="index">{{ tarea }}</li>
            <p>{{ nuevaTarea }}</p>
            <button @click="borrar">Borrar</button>
        </ul>
    </div>
</template>

<script setup>
import { ref } from 'vue';
const tareas = ref([]);
const nuevaTarea = ref('');
const addTarea = () => {
    tareas.value.push(nuevaTarea.value);
    nuevaTarea.value = '';
}
const borrar = (index) =>{
    tareas.value.splice(index, 1)
}

</script>

<style>
* {
    font-family: Arial, Helvetica, sans-serif;
}
div {
    text-align: center;
}
</style>