<script>
import feather from "feather-icons";
import Social from "./Social";

export default {
  components: {Social},
  data: () => {
    return {
      // Todo
    };
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
  <div class="py-60">
    <main id="skip" class="flex flex-col justify-between ">
      <div>
        <div style="opacity: 1;">
          <div class="flex flex-col-reverse sm:flex-row">
            <div class="w-full gap-4 sm:w-9/12">
              <h1 class=" museo-sans-bold mb-1 text-3xl text-gray-700 dark:text-gray-50 sm:text-4xl md:text-5xl ">Asraf Porag</h1>
              <h3 class=" museo-sans-regular mb-2 mt-2 text-lg text-neutral-700 dark:text-gray-50 ">Fullstack developer</h3>
              <p class=" museo-sans-regular animate-fade-in-down text-md text-neutral-600 dark:text-gray-50 ">PHP,JavaScript, 🤖 Laravel, Vue, React, Node, Express.</p>
              <social/>
            </div>
            <div class="profile-image mb-5 w-full p-0 sm:mb-0 sm:w-3/12 -mt-5">
              <div class="image-shadow ml-auto">
                <img alt="" aria-hidden="true" src="/images/asraf.jpg">
              </div>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

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

.profile-image .image-shadow{
  align-self: end;
  height: 200px;
  width: 200px;
  border-radius: 50%;
}
.profile-image .image-shadow img{
  height: 200px;
  width: 200px;
  border-radius: 50%;
}

</style>
