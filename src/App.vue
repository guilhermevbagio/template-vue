<script setup>
  import { ref } from 'vue';	
  let username;
  let senha;
  const savedLogin = ref('');
  const savedSenha = ref('');

  function saveLogin() {
    console.log("a");
    savedLogin.value = username;
    savedSenha.value = senha;
  }

</script>

<template>
  <div class="flex flex-col gap-4 justify-center items-center h-screen w-screen">
    <div class="shadow-md bg-slate-100 p-4 rounded-lg justify-center items-center flex flex-col">
      <div class="flex flex-col">
        <label for="login">Login</label>
        <input v-model="username" class="border border-slate-400 bg-white rounded h-8 px-2">
      </div>
      <div class="flex flex-col mt-2">
        <label for="senha">Senha</label>
        <input v-model="senha" type="password" class="border border-slate-500 bg-white rounded h-8 px-2">
      </div>
      <button class="flex justify-center items-center bg-green-800 px-4 h-8 mt-4 rounded w-full cursor-pointer shadow text-white hover:opacity-80 transition duration-150 will-change-auto" @click="saveLogin()">
        Enviar
      </button>
    </div>

    <div class="text-xl text-black text-center">
      {{ savedLogin }} <br>
      {{ savedSenha }}
    </div>
  </div>
</template>


