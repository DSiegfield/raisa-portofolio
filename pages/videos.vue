<template>
  <div class="relative flex flex-col items-center bg-base-200 gap-10 pb-10">
    <div class="hero bg-primary" style="">
      <div class="hero-content text-center">
        <div class="">
          <h1
            class="mb-5 text-6xl md:text-7xl lg:text-9xl font-bold text-black"
          >
            Videos
          </h1>
          <p class="text-white text-md lg:text-lg font-bold">
            Este é o primeiro story criado para o lançamento de uma marca, com o
            objetivo de despertar curiosidade e mistério. Na sua construção,
            utilizei o Adobe Express, com o bigode em destaque sendo gerado por
            IA e posteriormente editado para remover o fundo e aplicar um filtro
            esfumaçado, intensificando as sombras. As cores predominantes no
            vídeo, amarelo e preto, foram escolhidas propositalmente para
            refletir a paleta da marca, garantindo coerência visual com a
            identidade da logo.
          </p>
        </div>
      </div>
    </div>
    <div class="flex flex-col lg:flex-row gap-10">
      <div class="mockup-phone border-primary">
        <div class="camera"></div>
        <div class="display">
          <video class="h-96" controls>
            <source src="/videos/instagram.mp4" type="video/mp4" />
            Your browser does not support the video tag.
          </video>
        </div>
      </div>
      <div class="mockup-phone border-primary">
        <div class="camera"></div>
        <div class="display">
          <video class="h-96" controls>
            <source src="/videos/cativante.mp4" type="video/mp4" />
            Your browser does not support the video tag.
          </video>
        </div>
      </div>
    </div>
  </div>
</template>
