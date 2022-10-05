<script>
import { mapState } from "vuex";
import feather from "feather-icons";
import FooterCopyright from "./FooterCopyright.vue";
import Social from "./Social";
export default {
  components: {Social, FooterCopyright },
  data: () => {
    return {
      // Todo
    };
  },
  computed: {
    ...mapState(["copyrightDate", "socialProfiles"]),
  },
  mounted() {
    feather.replace();
  },
  updated() {
    feather.replace();
  },
};
</script>

<template>

  <footer class="sm:container sm:mx-auto p-4 sm:p-6 dark:bg-primary-dark bg-white">
    <div class="sm:flex sm:items-center sm:justify-between sm:mx-0 mx-24">
      <NuxtLink to="/">
        <span class="font-sans cursor-pointer bg-gradient-to-r from-blue-dark to-blue-light bg-clip-text text-2xl uppercase text-transparent sm:block">Asraf</span>
      </NuxtLink>
      <ul class="flex flex-wrap items-center mb-6 text-sm text-gray-500 sm:mb-0 dark:text-gray-400">
        <li>
          <a href="#" class="mr-4 hover:underline md:mr-6 ">About</a>
        </li>
        <li>
          <a href="#" class="mr-4 hover:underline md:mr-6">Privacy Policy</a>
        </li>
        <li>
          <a href="#" class="mr-4 hover:underline md:mr-6 ">Licensing</a>
        </li>
        <li>
          <a href="#" class="hover:underline">Contact</a>
        </li>
      </ul>
    </div>
    <hr class="my-6 border-gray-200 dark:border-gray-700 lg:my-8 sm:mx-0 mx-24">
    <div class="sm:flex sm:items-center sm:justify-between sm:mx-0 mx-24">
        <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400">© 2022 <a href="https://asrafporag.me/" target="_blank" class="hover:underline">Asraf Porag™</a>. All Rights Reserved.
        </span>
      <social></social>
    </div>
  </footer>
</template>

<style scoped></style>
