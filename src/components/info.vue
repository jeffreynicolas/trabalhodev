<script setup>
import { ref } from 'vue';
let nome = ref('')
let email = ref('')
let nascimento = ref(null)
defineProps(["senha", "Csenha"])
</script>

<template>

<div class="info">
      <div>
        <input type="text" v-model="nome" minlength="3" maxlength="20" placeholder="digite seu nome" />
        <input type="email" v-model="email" placeholder="digite seu email" />
        <input type="date" v-model="nascimento" placeholder="data de nascimento"/>
      </div>
      <div>
        <input required type="password" v-model="senha" placeholder="Senha" />
        <input required type="password" v-model="Csenha" placeholder="Confirmar Senha" />
      </div>
    </div>
</template>

<style scoped>
.info {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  border: 1px solid #575353;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  background-color: #beb5b5;
  color: #000000;
}
</style>
