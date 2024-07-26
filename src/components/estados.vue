<script setup>
import { ref } from 'vue';
    const SEst = ref("");
    defineProps(["estados"])
</script>

<template>
     <div class="estado">
      <select v-model="SEst">
        <option disabled value="">Selecione o estado</option>
        <option v-for="(estado, index) in estados" :key="index" :value="estado.id">
          {{ estado.name }}
        </option>
      </select>
      <span> {{ SEst }} </span>
    </div>
</template>

<style scoped>
.estado {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  border: 1px solid #3f3c3c;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  background-color: #beb5b5;
  color: #000000;
}
</style>