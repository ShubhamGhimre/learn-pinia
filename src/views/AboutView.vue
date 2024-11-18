<script setup>
import { useCounterStore } from "@/stores/counter";

const counterStore = useCounterStore();



</script>


<template>
  <div class="about">
     <h1>about</h1>
      <button @click="counterStore.increaseCount" class="counter-button"> 
        {{ counterStore.count }}
      </button>
   </div>
 </template>

 <style>
.counter-button {
  font-size: 20px;
  margin: 0 10px;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  background-color: #41b883;
  color: white;
  cursor: pointer;
}
  .about{
    text-align: center;
  }
</style>
 