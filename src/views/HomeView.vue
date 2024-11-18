<script setup>
// import { computed, ref } from "vue";
import Counter from "@/components/Counter.vue";
import { useCounterStore } from "@/stores/counter";

const storeCounter = useCounterStore();

</script>

<template>
  <div class="home">
    <counter />
    <div class="buttons">
      <button @click="storeCounter.decreaseCount">-</button>
      <button @click="storeCounter.increaseCount">+</button>
    </div>
    <hr>
    <div>
      This counter is: {{ storeCounter.oddOrEven }} 
    </div>
    <hr>
    <div>
      <h3>Edit Counter</h3>
      <input type="number" model="storeCounter.count">
    </div>
  </div>
</template>

<style>
.count {
  font-size: 60px;
  margin: 20px;
  color: #41b883;
}
.buttons {
  display: flex;
  justify-content: center;
  gap: 20px;
}
.buttons button {
  font-size: 20px;
  margin: 0 10px;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  background-color: #41b883;
  color: white;
  cursor: pointer;
}
</style>
