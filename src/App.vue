<template>
  <!-- Wrapper -->
  <div class="w-full h-screen flex justify-center items-center bg-gray-200">
    <!-- Main-Div -->
    <div class="shadow-lg rounded-lg p-4 bg-white dark:bg-black dark:text-white space-y-3">
      <!-- Header -->
      <div class="flex justify-between items-center">
        <!-- Heading -->
        <h1 class="text-2xl font-semibold">
          Hey, i'am Shahbaz
        </h1>
        <!--/ Heading -->

        <!-- Toggle-Button -->
        <div>
          <button @click="toggleBtn()" type="button">
            <MoonIcon v-if="isDark" class="w-7" /> <!-- When DarkMode -->
            <SunIcon v-else class="w-7" /> <!-- When LightMode -->
          </button>
        </div>
        <!--/ Toggle-Button -->
      </div>
      <!--/ Header -->

      <!-- Paragraph -->
      <p>
        A full-stack web-application developer.
        <br>
        The dark and light mode application using
        <a href="https://vuejs.org" target="_blank" class="bg-gray-100 px-1 pb-1 rounded dark:bg-black">
          vue-js
        </a>,
        <a href="https://vueuse.org" target="_blank" class="bg-gray-100 px-1 pb-1 rounded dark:bg-black">
          tailwind-css
        </a> and
        <a href="https://tailwindcss.com" target="_blank" class="bg-gray-100 px-1 pb-1 rounded dark:bg-black">
          vue-use
        </a>
      </p>
      <!--/ Paragraph -->
      <hr>
      <!-- UI-Buttons -->
      <div>
        <button type="button"
          class="px-4 py-1 bg-blue-700 text-white rounded-lg hover:bg-blue-800 active:bg-blue-700 mr-3">
          Download
        </button>
        <button type="button"
          class="px-4 py-1 bg-gray-100 rounded-lg hover:bg-gray-200 active:bg-gray-100 border dark:text-black">
          Save
        </button>
      </div>
      <!--/ UI-Buttons -->
    </div>
    <!--/ Main-Div -->
  </div>
  <!--/ Wrapper -->
</template>

<script setup>
/* Import Solid-HeroIcons */
import { SunIcon, MoonIcon } from "@heroicons/vue/24/solid";

/* Import VueUse-Library */
import { useDark, useToggle } from '@vueuse/core';

const isDark = useDark();
const toggleBtn = useToggle(isDark);
</script>
