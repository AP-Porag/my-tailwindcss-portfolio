<template>
  <div class="">
    <div class="block sm:flex sm:gap-10 mt-10 sm:mt-20">
      <!-- About profile image -->
      <div class="profile-image w-full sm:w-1/4 mb-7 sm:mb-0">
        <div class="image-shadow">
          <img src="/images/asraf.jpg" class="rounded-lg w-96" alt="" />
        </div>
      </div>

      <!-- About details -->
      <div class="w-full sm:w-3/4 text-left">
        <p
          v-for="bio in aboutMe"
          :key="bio.id"
          class="
          font-general-regular
          mb-4
          text-ternary-dark
          dark:text-ternary-light
          text-lg
        "
        >
          {{ bio.bio }}
        </p>
      </div>
    </div>
    <div class="block sm:flex sm:gap-10 mt-10 sm:mt-20">
      <!-- About profile image -->
      <div class="w-full sm:w-1/4 mb-7 sm:mb-0">
        <h1 class="general-sans-medium rounded-sm border-l-4 border-neutral-100 pl-3 text-2xl sm:text-3xl text-neutral-700 dark:border-secondary-dark dark:text-ternary-light ">Employment</h1>
      </div>

      <!-- About details -->
      <div class="w-full sm:w-3/4 text-left">


        <ol class="relative border-l border-gray-200 dark:border-gray-700">
          <li class="mb-10 ml-6" v-for="employment in employments" :key="employment.id">
        <span class="flex absolute -left-3 justify-center items-center w-6 h-6 bg-blue-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-blue-900">
            <svg aria-hidden="true" class="w-3 h-3 text-blue-600 dark:text-blue-400" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"></path></svg>
        </span>
<!--            <h5 class="text-md font-bold mb-2 text-gray-800">{{employment.designation}}</h5>-->
<!--            <p class="text-gray-700"><span>{{employment.company}}</span>  <span>{{employment.address}}</span></p>-->
<!--            <p class="text-gray-700"><span>{{employment.start +' - '+employment.end}}</span></p>-->
            <div class="bg-white p-6 rounded-lg shadow-lg mb-5">
              <h5 class="text-md font-bold mb-2 text-gray-800">{{employment.designation}}</h5>
              <p class="text-gray-700"><span>{{employment.company}}</span>  <span>{{employment.address}}</span></p>
              <p class="text-gray-700"><span>{{employment.start +' - '+employment.end}}</span></p>
            </div>
          </li>
        </ol>
        <div class="flex justify-center sm:block">
          <a
            href="/Asraf-Resume.pdf"
            download=""
            class="
            flex
            justify-center
            items-center
            w-36
            sm:w-48
            mt-12
            mb-6
            sm:mb-0
            text-lg
            border border-indigo-200
            dark:border-ternary-dark
            py-2.5
            sm:py-3
            shadow-lg
            rounded-lg
            bg-indigo-50
            focus:ring-1 focus:ring-indigo-900
            hover:bg-indigo-500
            text-gray-500
            hover:text-white
            duration-500
          "
            aria-label="Download Resume"
          >
            <i
              data-feather="arrow-down-circle"
              class="ml-0 sm:ml-1 mr-2 sm:mr-3 w-5 sm:w-6 duration-100"
            ></i>
            <span class="text-sm sm:text-lg font-general-medium duration-100"
            >Download CV</span
            ></a
          >
        </div>
      </div>
    </div>
  </div>

</template>
<script>
import { mapState } from "vuex";

export default {
  data: () => {
    return {
      // @todo
      employments:[
        {'id':'1','designation':'Full Stack Developer','company':'IT-Clan BD','address':'Dhaka, Bangladesh','start':'Jan 2022','end':'Present'},
        {'id':'2','designation':'Web Administrator','company':'Gul Istanbul ','address':'Kabul, Istanbul','start':'Feb 2017','end':'Dec 2017'},
      ]
    };
  },
  computed: {
    ...mapState(["aboutMe"]),
  },
};
</script>
<style scoped>
.profile-image {
  display: flex;
  justify-content: left;
  z-index: 999;
}
.profile-image .image-shadow {
  position: relative;
  text-align: center;
}
.profile-image .image-shadow:after {
  position: absolute;
  content: "";
  top: 3vw;
  left: 0;
  right: 0;
  z-index: -1;
  height: 100%;
  width: 100%;
  margin: 0 auto;
  transform: scale(.6);
  -moz-filter: blur(5vw);
  -ms-filter: blur(5vw);
  filter: blur(5vw);
  background: linear-gradient(270deg,#335eea,#1a9dfe,#ce2e39);
  background-size: 200% 200%;
  -webkit-animation: animateBgColors 10s ease infinite;
  animation: animateBgColors 10s ease infinite;
}


</style>
