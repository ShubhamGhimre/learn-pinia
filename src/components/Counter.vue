<script setup>
// import { computed, ref } from "vue";
import { useCounterStore } from "@/stores/counter";

const storeCounter = useCounterStore();

</script>

<template>
     <div class="count">
      {{ storeCounter.$state.count }}
    </div>
</template>