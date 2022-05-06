<script setup lang="ts">
import { ref } from "vue";
import { uiType } from "./ui";

const { title, variant } = defineProps<{
  title: string;
  variant?: string;
}>();

const buttonType = ref(uiType(variant));

const classes = [
  "px-4 py-2 text-white transition duration-100 ease-in-out bg-blue-500 border border-transparent rounded shadow-sm hover:bg-blue-600 focus:border-blue-500 focus:ring-2 focus:ring-blue-500 focus:outline-none focus:ring-opacity-50 disabled:opacity-50 disabled:cursor-not-allowed",

  "px-4 py-2 text-black transition duration-100 ease-in-out bg-gray-100 border border-transparent rounded shadow-sm hover:bg-blue-600 focus:border-blue-500 focus:ring-2 focus:ring-blue-500 focus:outline-none focus:ring-opacity-50 disabled:opacity-50 disabled:cursor-not-allowed",

  "px-4 py-2 text-black transition duration-100 ease-in-out bg-red-600 border border-transparent rounded shadow-sm hover:bg-blue-600 focus:border-blue-500 focus:ring-2 focus:ring-blue-500 focus:outline-none focus:ring-opacity-50 disabled:opacity-50 disabled:cursor-not-allowed",
];
</script>

<template>
  <button :class="classes[buttonType]">
    {{ title }}
  </button>
</template>
