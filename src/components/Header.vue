<script setup>
import VueFeather from "vue-feather";
import { links } from "../utils/constant";
</script>

<template>
  <header>
    <nav class="bg-gray-50 px-4 md:px-6 py-4">
      <div
        class="flex flex-wrap justify-center md:justify-between items-center mx-auto max-w-screen-xl"
      >
        <div class="self-center text-xl font-semibold whitespace-nowrap">
          Basic Vue
        </div>
        <div
          class="justify-center md:justify-between items-center w-full flex md:w-auto md:order-1"
        >
          <ul class="flex mt-4 md:gap-x-8 md:mt-0">
            <li v-for="(link, index) in links" :key="index">
              <router-link
                active-class="text-black"
                :to="link.href"
                class="flex items-center gap-1 py-2 pr-4 pl-3 text-gray-500 hover:text-gray-600 md:p-0 transition"
              >
                <vue-feather :type="link.icon" class="w-4 h-4" />

                {{ link.name }}
              </router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>
