<script setup>
import { ref } from 'vue';
import infocomponent from './components/info.vue';
import estadocomponent from './components/estados.vue';
import shobcomponent from './components/Shob.vue';
import SLingingcomponent from './components/ling.vue';

    let bio = ref("")
    const senha = ref('senha');
    const Csenha = ref('Csenha');
    const SLing = ref([]);

    const estados = ref([
      { id: "Acre", name: "AC" },
      { id: "Alagoas", name: "AL" },
      { id: "Amapá", name: "AP" },
      { id: "Amazonas", name: "AM" },
      { id: "Bahia", name: "BA" },
      { id: "Ceará", name: "CE" },
      { id: "Distrito Federal", name: "DF" },
      { id: "Espírito Santo", name: "ES" },
      { id: "Goiás", name: "GO" },
      { id: "Maranhão", name: "MA" },
      { id: "Mato Grosso", name: "MT" },
      { id: "Mato Grosso do Sul", name: "MS" },
      { id: "Minas Gerais", name: "MG" },
      { id: "Pará", name: "PA" },
      { id: "Paraíba", name: "PB" },
      { id: "Paraná", name: "PR" },
      { id: "Pernambuco", name: "PE" },
      { id: "Piauí", name: "PI" },
      { id: "Rio de Janeiro", name: "RJ" },
      { id: "Rio Grande do Norte", name: "RN" },
      { id: "Rio Grande do Sul", name: "RS" },
      { id: "Rondônia", name: "RO" },
      { id: "Roraima", name: "RR" },
      { id: "Santa Catarina ",name: "SC" },
      { id: "São Paulo", name: "SP" },
      { id: "Sergipe", name: "SE" },
      { id: "Tocantins", name: "TO" },
    ]);

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

    const linguagens = ref([
      { id: "Python", name: "Python" },
      { id: "JavaScript", name: "JavaScript" },
      { id: "Java", name: "Java" },
      { id: "C++", name: "C++" },
      { id: "Ruby", name: "Ruby" },
    ]);

    const Vsenha = () => {
      if (senha.value === Csenha.value) {
        return true;
      } else {
        alert("As senhas não são iguais");
        return false;
      }
    };

    const enviar = () => {
      if (Vsenha()) {
        const info = {
          nome: nome.value,
          email: email.value,
          nascimento: nascimento.value,
          estado: SEst.value,
          hob: SHob.value,
          linguagens: SLing.value,
          biografia: bio.value,
        };
        alert(`Informações: \n${JSON.stringify(info, null, 2)}`);
      }
    };
</script>

<template>
  <form @submit.prevent="enviar">
<infocomponent :senha="senha" :Csenha="Csenha"/>  
<estadocomponent :estado="estados"/>
<shobcomponent :SHob="Shob"/>


   
  </form>
</template>

<style>




button[type="submit"] {
  background-color: #4d504d;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button[type="submit"]:hover {
  background-color: #676b67;
}
</style>