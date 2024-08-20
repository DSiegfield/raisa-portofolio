<script setup lang="ts">
import {
  galleryImages,
  initialImage,
  type imageGalleryType,
} from "@/data/images";

// Get references to elements
// const gallery = ref();
// const lightbox = ref();
// const lightboxImage = ref();
// const closeButton = ref();

const images = ref(galleryImages);

const imagesClass =
  "gallery-image object-cover rounded-3xl hover:grayscale transition-all duration-700 ease-in-out mx-auto w-full h-full animate-pulse-glow";

let selectedImage = ref(initialImage);

const showModal = ref(false);

const openModal = (id: number): void => {
  console.log("here", id);
  const image = images.value.find((image) => image.id === id);
  console.log(image);
  if (!image) return;
  selectedImage.value = image;
  showModal.value = true;
};

const closeModal = (): void => {
  showModal.value = false;
  selectedImage.value = initialImage;
};
</script>

<template>
  <!-- Custom Style -->

  <section class="py-24">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="gallery" ref="gallery">
        <div class="flex flex-col mb-10">
          <div class="grid md:grid-cols-12 gap-8 lg:mb-11 mb-7">
            <div
              class="md:col-span-8 md:h-[404px] h-[277px] w-full rounded-3xl"
            >
              <img
                :src="images[0].src"
                :alt="images[0].alt"
                :class="imagesClass"
                @click="openModal(0)"
              />
            </div>
            <div
              class="md:col-span-4 md:h-[404px] h-[277px] w-full rounded-3xl"
            >
              <NuxtImg
                :src="images[1].src"
                :alt="images[1].alt"
                :class="imagesClass"
                @click="openModal(1)"
              />
            </div>
          </div>

          <div class="grid md:grid-cols-12 gap-8 lg:mb-11 mb-7">
            <div class="md:col-span-4 md:h-full w-full rounded-3xl">
              <NuxtImg
                :src="images[2].src"
                :alt="images[2].alt"
                :class="imagesClass"
                @click="openModal(2)"
              />
            </div>
            <div class="md:col-span-4 md:h-full w-full rounded-3xl">
              <NuxtImg
                :src="images[3].src"
                :alt="images[3].alt"
                :class="imagesClass"
                @click="openModal(3)"
              />
            </div>
            <div class="md:col-span-4 md:h-full w-full rounded-3xl">
              <NuxtImg
                :src="images[4].src"
                :alt="images[4].alt"
                :class="imagesClass"
                @click="openModal(4)"
              />
            </div>
          </div>

          <div class="grid md:grid-cols-12 gap-8 lg:mb-11 mb-7">
            <div class="md:col-span-4 md:h-full w-full rounded-3xl">
              <NuxtImg
                :src="images[7].src"
                :alt="images[7].alt"
                :class="imagesClass"
                @click="openModal(7)"
              />
            </div>
            <div class="md:col-span-8 md:h-full w-full rounded-3xl">
              <NuxtImg
                :src="images[6].src"
                :alt="images[6].alt"
                :class="imagesClass"
                @click="openModal(6)"
              />
            </div>
          </div>

          <div class="grid md:grid-cols-12 gap-8 lg:mb-11 mb-7">
            <div class="md:col-span-6 md:h-full w-full rounded-3xl">
              <NuxtImg
                :src="images[8].src"
                :alt="images[8].alt"
                :class="imagesClass"
                @click="openModal(8)"
              />
            </div>
            <div class="md:col-span-6 md:h-full w-full rounded-3xl">
              <NuxtImg
                :src="images[9].src"
                :alt="images[9].alt"
                :class="imagesClass"
                @click="openModal(9)"
              />
            </div>
          </div>

          <div class="grid md:grid-cols-12 gap-8 lg:mb-11 mb-7">
            <div class="md:col-span-6 md:h-full w-full rounded-3xl">
              <NuxtImg
                :src="images[10].src"
                :alt="images[10].alt"
                :class="imagesClass"
                @click="openModal(10)"
              />
            </div>
            <div class="md:col-span-6 md:h-full w-full rounded-3xl">
              <NuxtImg
                :src="images[11].src"
                :alt="images[11].alt"
                :class="imagesClass"
                @click="openModal(11)"
              />
            </div>
          </div>
        </div>
      </div>
    </div>

    <dialog
      class="lightbox flex justify-center p-10 backdrop-blur-sm"
      id="lightbox"
      ref="lightbox"
      v-if="showModal"
    >
      <div class="card w-full flex justify-center">
        <figure>
          <img
            :src="selectedImage.src"
            :alt="selectedImage.alt"
            class="lightbox-image"
            id="lightbox-image"
            ref="lightboxImage"
          />
        </figure>
        <div class="card-body">
          <h1 class="card-title text-2xl">{{ selectedImage.name }}</h1>
          <p>{{ selectedImage.description }}?</p>
          <div class="card-actions justify-end">
            <button class="btn btn-primary" @click="closeModal">Fechar</button>
          </div>
        </div>
      </div>
    </dialog>
  </section>
  <!-- Initialize Swiper -->
</template>

<style scoped>
.lightbox {
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

@keyframes pulse-glow {
  0%,
  100% {
    box-shadow: 0 0 10px 2px rgba(255, 255, 255, 0.5);
  }
  50% {
    box-shadow: 0 0 20px 4px rgba(255, 255, 255, 1);
  }
}

.animate-pulse-glow {
  animation: pulse-glow 2s infinite ease-in-out;
}
</style>
