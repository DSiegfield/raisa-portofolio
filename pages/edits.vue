<script setup>
const images = ref([
  {
    id: 0,
    title: "Pessoa a beira da piscina",
    description:
      "Esta foto foi editada no Photoshop, empregando a ferramenta de Filtros Neurais para suavizar a pele e garantir um acabamento mais uniforme. Adicionalmente, utilizei as ferramentas de retoque para ajustar o contraste e aprimorar a iluminação da imagem, resultando em uma aparência mais vibrante e equilibrada.",
    antes: "/images/piscina_antes.jpg",
    depois: "/images/piscina_depois.jpg",
  },
  {
    id: 1,
    title: "Paisagem antes da edição",
    description:
      "Este exercício, parte de um curso na Udemy, envolveu a geração de elementos utilizando o Fill Generator do Photoshop e a seleção precisa da área onde o elemento deveria ser posicionado. A imagem mostra o resultado antes e depois da edição, ilustrando o processo de integração e personalização dos elementos.",
    antes: "/images/paisagem.jpg",
    depois: "/images/paisagem_edit.png",
  },
]);
</script>

<template>
  <div class="relative flex flex-col items-center bg-base-200 gap-10 pb-10">
    <div class="hero bg-primary" style="">
      <div class="hero-content text-center">
        <div class="">
          <h1
            class="mb-5 text-6xl md:text-7xl lg:text-9xl font-bold text-black"
          >
            Antes VS Depois
          </h1>
        </div>
      </div>
    </div>
    <div v-for="image in images" :key="image.id" class="w-5/6">
      <DiffImage
        :title="image.title"
        :description="image.description"
        :image-src-antes="image.antes"
        :image-src-depois="image.depois"
      />
    </div>
  </div>
</template>
