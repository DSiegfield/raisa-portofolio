<script setup>
// Get references to elements
const gallery = ref();
const lightbox = ref();
const lightboxImage = ref();
const closeButton = ref();

const showModal = ref(false);

// Define the openLightbox function
const openLightbox = (e) => {
  if (e.target.classList.contains("gallery-image")) {
    const imageSrc = e.target.src;
    lightboxImage.value.src = imageSrc;
    lightbox.value.style.display = "flex";
  }
};

onMounted(() => {
  // Add event listener to each image
  gallery.value.addEventListener("click", openLightbox);
});

onBeforeUnmount(() => {
  gallery.value.removeEventListener("click", openLightbox);
});
</script>

<template>
  <!-- Custom Style -->

  <section class="py-24">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="gallery" ref="gallery">
        <div class="flex flex-col mb-10">
          <!-- <div class="grid md:grid-cols-12 gap-8 lg:mb-11 mb-7">
            <div
              class="md:col-span-4 md:h-[404px] h-[277px] w-full rounded-3xl"
            >
              <img
                src="https://pagedone.io/asset/uploads/1713942989.png"
                alt="Gallery image"
                class="gallery-image object-cover rounded-3xl hover:grayscale transition-all duration-700 ease-in-out mx-auto lg:col-span-4 md:col-span-6 w-full h-full"
              />
            </div>
            <div
              class="md:col-span-8 md:h-[404px] h-[277px] w-full rounded-3xl"
            >
              <img
                src="https://pagedone.io/asset/uploads/1713943004.png"
                alt="Gallery image"
                class="gallery-image object-cover rounded-3xl hover:grayscale transition-all duration-700 ease-in-out mx-auto lg:col-span-8 md:col-span-6 w-full h-full"
              />
            </div>
          </div>
          <div class="grid md:grid-cols-3 grid-cols-1 gap-8">
            <div class="h-[277px] w-full rounded-3xl">
              <img
                src="https://pagedone.io/asset/uploads/1713943024.png"
                alt="Gallery image"
                class="gallery-image object-cover rounded-3xl hover:grayscale transition-all duration-700 ease-in-out mx-auto w-full h-full"
              />
            </div>
            <div class="h-[277px] w-full rounded-3xl">
              <img
                src="https://pagedone.io/asset/uploads/1713943039.png"
                alt="Gallery image"
                class="gallery-image object-cover rounded-3xl hover:grayscale transition-all duration-700 ease-in-out mx-auto w-full h-full"
              />
            </div>
            <div class="h-[277px] w-full rounded-3xl">
              <img
                src="https://pagedone.io/asset/uploads/1713943054.png"
                alt="Gallery image"
                class="gallery-image object-cover rounded-3xl hover:grayscale transition-all duration-700 ease-in-out mx-auto w-full h-full"
              />
            </div>
          </div> -->
          <div class="grid md:grid-cols-12 gap-8 lg:mb-11 mb-7">
            <div
              class="md:col-span-8 md:h-[404px] h-[277px] w-full rounded-3xl"
            >
              <img
                src="/images/bg_jarbas.png"
                class="gallery-image object-cover rounded-3xl hover:grayscale transition-all duration-700 ease-in-out mx-auto w-full h-full"
                @click="showModal = true"
              />
            </div>
            <div
              class="md:col-span-4 md:h-[404px] h-[277px] w-full rounded-3xl"
            >
              <img
                src="/images/depoimentos_de_clientes.png"
                class="gallery-image object-cover rounded-3xl hover:grayscale transition-all duration-700 ease-in-out mx-auto w-full h-full"
                @click="showModal = true"
              />
            </div>
          </div>
          <div class="grid md:grid-cols-12 gap-8 lg:mb-11 mb-7">
            <div class="md:col-span-4 md:h-full w-full rounded-3xl">
              <img
                src="/images/Enquete_mobilidade_post_dia_2.png"
                alt="Gallery image"
                class="gallery-image object-cover rounded-3xl hover:grayscale transition-all duration-700 ease-in-out mx-auto w-full h-full"
                @click="showModal = true"
              />
            </div>
            <div class="md:col-span-4 md:h-full w-full rounded-3xl">
              <img
                src="/images/Enquete_mobilidade3.png"
                alt="Gallery image"
                class="gallery-image object-cover rounded-3xl hover:grayscale transition-all duration-700 ease-in-out mx-auto w-full h-full"
                @click="showModal = true"
              />
            </div>
            <div class="md:col-span-4 md:h-full w-full rounded-3xl">
              <img
                src="/images/Celular_iPhone_11_Mockup_PSD_logo.png"
                alt="Gallery image"
                class="gallery-image object-cover rounded-3xl hover:grayscale transition-all duration-700 ease-in-out mx-auto w-full h-full"
                @click="showModal = true"
              />
            </div>
          </div>
        </div>
      </div>
    </div>

    <div
      class="lightbox flex justify-center p-10 backdrop-blur-sm"
      id="lightbox"
      ref="lightbox"
      v-if="showModal"
    >
      <div class="card w-full">
        <figure>
          <img
            src=""
            alt=""
            class="lightbox-image"
            id="lightbox-image"
            ref="lightboxImage"
          />
        </figure>
        <div class="card-body">
          <h2 class="card-title">Life hack</h2>
          <p>How to park your car at your garage?</p>
          <div class="card-actions justify-end">
            <button class="btn btn-primary">Learn now!</button>
          </div>
        </div>
      </div>
      <span
        class="close"
        id="close"
        ref="closeButton"
        @click="showModal = false"
        >&times;</span
      >
      <!-- <img
        src=""
        alt=""
        class="lightbox-image"
        id="lightbox-image"
        ref="lightboxImage"
      /> -->
    </div>
  </section>
  <!-- Initialize Swiper -->
</template>

<style>
.lightbox {
  display: none;
  position: fixed;
  z-index: 999;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  background-color: rgba(0, 0, 0, 0.8);
}
.lightbox-image {
  display: block;
  margin: auto;
  max-width: 100%;
  max-height: 100%;
}
.close {
  color: #fff;
  font-size: 3em;
  position: absolute;
  top: 20px;
  right: 30px;
  cursor: pointer;
}
.gallery {
  width: 90vw;
  max-width: 1200px;
  margin: 0 auto;
  grid-template-rows: 1fr;
  grid-column-gap: 30px;
  grid-row-gap: 30px;
}
.gallery img {
  max-width: 100%;
  cursor: pointer;
}
.gallery img:hover {
  max-width: 100%;
  cursor: pointer;
}
</style>
