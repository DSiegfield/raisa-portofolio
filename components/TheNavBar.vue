<script setup>
import { computed } from "vue";
import { useRoute } from "nuxt/app";

const route = useRoute();
const isDropdownActive = ref(false);

const buttons = ref([
  {
    title: "Home",
    path: "/",
  },
  {
    title: "Sobre Mim",
    path: "/sobre",
  },
  {
    title: "Galeria",
    path: "/galeria",
  },
  {
    title: "Edits",
    path: "/edits",
  },
  {
    title: "Animações",
    path: "/anime",
  },
  {
    title: "Videos",
    path: "/videos",
  },
]);

const getLinkClass = (path) => {
  return computed(() =>
    route.path === path || route.path === path + "/"
      ? "btn-primary"
      : "btn-ghost"
  );
};
</script>

<template>
  <div
    class="navbar bg-base-100 flex-row-reverse justify-around lg:flex lg:flex-row gap-5"
  >
    <div class="avatar mx-3">
      <div
        class="ring-primary ring-offset-base-100 w-24 rounded-full ring ring-offset-2"
      >
        <NuxtImg src="/images/profile.jpg" alt="profile" />
      </div>
    </div>
    <h1
      class="bg-gradient-to-r from-primary via-violet-600 to-secondary inline-block text-3xl text-transparent bg-clip-text font-bold font-newpacifico"
      style="line-height: 2"
    >
      Raisa Designs
    </h1>
    <div class="dropdown lg:hidden">
      <div tabindex="0" role="button" class="btn m-1 bg-primary text-white">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="size-6"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3.75 5.25h16.5m-16.5 4.5h16.5m-16.5 4.5h16.5m-16.5 4.5h16.5"
          />
        </svg>
      </div>
      <ul
        tabindex="0"
        class="dropdown-content menu bg-primary rounded-box z-[99] w-52 p-2 shadow text-white bg-opacity-25 backdrop-blur-sm"
      >
        <div v-for="button in buttons">
          <NuxtLink
            :class="getLinkClass(button.path).value"
            class="btn text-xl w-full"
            :to="button.path"
          >
            {{ button.title }}
          </NuxtLink>
        </div>
      </ul>
    </div>
    <div class="hidden lg:flex flex-1">
      <div v-for="button in buttons">
        <NuxtLink
          :class="getLinkClass(button.path).value"
          class="btn text-xl"
          :to="button.path"
        >
          {{ button.title }}
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
