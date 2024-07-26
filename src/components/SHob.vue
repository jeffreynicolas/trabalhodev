<script setup>
import { ref } from 'vue';
const SHob = ref([]);
defineProps(["Shob"]);

const hobs = ref([
      { id: "Futebol", name: "Futebol" },
      { id: "Basquete", name: "Basquete" },
      { id: "Volei", name: "Volei" },
      { id: "Tênis", name: "Tênis" },
      { id: "Pesca", name: "Pesca" },
      { id: "Pintura", name: "Pintura" },
      { id: "Livros", name: "Livros" },
      { id: "Robotica", name: "Robotica" },
      { id: "Programação", name: "Programação" },
      { id: "Natação", name: "Natação" },
    ]);
</script>

<template>
    <div class="hobs">
      <label>Qual seu hob</label>
      <div v-for="(hob, index) in hobs" :key="index">
        <input type="checkbox" v-model="SHob" :value="hob.id" :id="hob.id" />
        <label :for="hob.id">{{ hob.name }}</label>
      </div>
      <span> {{ SHob }} </span>
    </div>

</template>

<style scoped>
.hobs {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  border: 1px solid #555151;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  background-color: #beb5b5;
  color: #000000;
}
</style>