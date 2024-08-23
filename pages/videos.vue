<template>
  <div class="relative flex flex-col items-center bg-base-200 gap-10 pb-10">
    <div class="hero bg-primary" style="">
      <div class="hero-content text-center">
        <div class="">
          <h1
            class="mb-5 text-6xl md:text-7xl lg:text-9xl font-bold text-black font-newpacifico"
          >
            Videos
          </h1>
          <p class="text-white text-md lg:text-xl font-bold font-comfortaa">
            Os vídeos apresentados aqui foram criados no Clipchamp e no Adobe
            Express, utilizando imagens geradas por IA e artes previamente
            fornecidas. Foram inseridos prints da aplicação e frames gerados por
            IA, além da aplicação de técnicas como efeitos de luz, zoom e
            filtros esfumaçados. As cores utilizadas seguem a paleta da marca,
            garantindo que o resultado final seja visualmente impactante
            e bem elaborado (2024).
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
