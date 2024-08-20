<template>
  <div class="hero min-h-screen bg-paisagem">
    <div class="hero-overlay bg-opacity-70"></div>
    <div class="hero-content text-neutral-content text-center">
      <div class="max-w-md">
        <h1 class="mb-5 text-5xl font-bold">Olá !</h1>
        <p class="mb-5 text-3xl">
          Este website foi construido para publicar os meus trabalhos
        </p>
        <button class="btn btn-primary text-xl" @click="navigateTo('/sobre')">
          Ver Perfil
        </button>
      </div>
    </div>
  </div>
</template>
