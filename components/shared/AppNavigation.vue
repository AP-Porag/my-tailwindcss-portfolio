<template>
  <!-- App header navigation links -->
  <div
    :class="isOpen ? 'block' : 'hidden'"
    class="
      m-0
      sm:ml-4
      mt-5
      sm:mt-3 sm:flex
      p-5
      sm:p-0
      justify-center
      items-center
      shadow-lg
      sm:shadow-none
    "
  >
    <NuxtLink
      :to="menu.route"
      class="
        block
        text-left
        text-lg
        text-gray-500
        font-medium
        dark:text-gray-500
        sm:mx-4
        mb-2
        sm:py-2
        border-t-2
        pt-3
        sm:pt-2 sm:border-t-0
        border-primary-light
        hover:text-blue-dark
        dark:border-secondary-dark
        capitalize
      "
      :aria-label="menu.area"
      v-for="menu in menus" :key="menu.id"
    ><span class="link link-underline link-underline-black"> {{menu.name}}</span>
    </NuxtLink>
<!--    <NuxtLink-->
<!--      to="/about"-->
<!--      class="-->
<!--        block-->
<!--        text-left text-lg text-primary-dark-->
<!--        dark:text-ternary-light-->
<!--        hover:text-secondary-dark-->
<!--        dark:hover:text-secondary-light-->
<!--        sm:mx-4-->
<!--        mb-2-->
<!--        sm:py-2-->
<!--        border-t-2-->
<!--        pt-3-->
<!--        sm:pt-2 sm:border-t-0-->
<!--        border-primary-light-->
<!--        dark:border-secondary-dark-->
<!--      "-->
<!--      aria-label="About Me"-->
<!--    >About</NuxtLink-->
<!--    >-->
<!--    <NuxtLink-->
<!--      to="/service"-->
<!--      class="-->
<!--        block-->
<!--        text-left text-lg text-primary-dark-->
<!--        dark:text-ternary-light-->
<!--        hover:text-secondary-dark-->
<!--        dark:hover:text-secondary-light-->
<!--        sm:mx-4-->
<!--        mb-2-->
<!--        sm:py-2-->
<!--      "-->
<!--      aria-label="Projects"-->
<!--    >Service</NuxtLink-->
<!--    >-->
<!--    <NuxtLink-->
<!--      to="/projects"-->
<!--      class="-->
<!--        block-->
<!--        text-left text-lg text-primary-dark-->
<!--        dark:text-ternary-light-->
<!--        hover:text-secondary-dark-->
<!--        dark:hover:text-secondary-light-->
<!--        sm:mx-4-->
<!--        mb-2-->
<!--        sm:py-2-->
<!--      "-->
<!--      aria-label="Projects"-->
<!--      >Projects</NuxtLink-->
<!--    >-->
<!--    <NuxtLink-->
<!--      to="/contact"-->
<!--      class="-->
<!--        block-->
<!--        text-left text-lg text-primary-dark-->
<!--        dark:text-ternary-light-->
<!--        hover:text-secondary-dark-->
<!--        dark:hover:text-secondary-light-->
<!--        sm:mx-4-->
<!--        mb-2-->
<!--        sm:py-2-->
<!--        border-t-2-->
<!--        pt-3-->
<!--        sm:pt-2 sm:border-t-0-->
<!--        border-primary-light-->
<!--        dark:border-secondary-dark-->
<!--      "-->
<!--      aria-label="Contact"-->
<!--      >Contact</NuxtLink-->
<!--    >-->
    <div
      class="
        font-general-regular
        border-t-2
        pt-3
        sm:pt-0 sm:border-t-0
        border-primary-light
        dark:border-secondary-dark
      "
    >
      <button
        class="
          sm:hidden
          block
          text-left text-md
          bg-gradient-to-r
          from-blue-dark
          to-blue-light
          hover:to-blue-dark
          hover:from-blue-light
          text-white
          shadow-xl
          rounded-md
          px-4
          py-2
          mt-2
        "
        @click="showModal()"
        aria-label="Hire Me Button"
      >
        Hire Me
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: ["isOpen", "showModal", "modal", "categories"],
  data(){
    return{
      menus:[
        {'id':'1','name':'home','route':'/','area':'Home'},
        {'id':'2','name':'about','route':'/about','area':'About'},
        {'id':'3','name':'services','route':'/services','area':'Services'},
        {'id':'4','name':'projects','route':'/projects','area':'Projects'},
        // {'id':'5','name':'articles','route':'/articles','area':'Articles'},
        {'id':'6','name':'contact','route':'/contact','area':'Contact'},
      ]
    }
  }
};
</script>

<style>
/*#nav .nuxt-link-exact-active,*/
/*#nav .nuxt-link-active {*/
/*  @apply text-blue-dark dark:text-blue-light;*/
/*}*/
#nav .nuxt-link-exact-active{
  @apply text-blue-dark dark:text-blue-light;
}
.link-underline {
  border-bottom-width: 0;
  background-image: linear-gradient(transparent, transparent), linear-gradient(#fff, #fff);
  background-size: 0 3px;
  background-position: 0 100%;
  background-repeat: no-repeat;
  transition: background-size .5s ease-in-out;
}

.link-underline-black {
  background-image: linear-gradient(transparent, transparent), linear-gradient(#0E6FBC, #2CC3FC)
}

.link-underline:hover {
  background-size: 100% 3px;
  background-position: 0 100%
}
</style>
