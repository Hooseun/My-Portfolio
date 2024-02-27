<template>
  <slot>
  <div
    class="h-[55.8rem] bg-[#111827] flex flex-row justify-center items-center"
  >
    <div class="flex flex-col w-5/6 h-5/6 items-center">
      <h1 class="text-white mt-10 font-bold text-[3.5rem]">
        CONTACT <span class="text-amber-300">ME</span>
      </h1>
      <p class="mt-6 w-[40rem] text-center text-[#6B7280]">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Error molestias
        obcaecati saepe totam nam tempore?
      </p>
      <div class="w-full h-full flex flex-row">
        <div class="flex flex-col w-1/2 justify-center items-center space-y-6">
          <h1 class="text-amber-300 font-bold">
            Contact Email:
            <NuxtLink to="/secret" class="text-white"
              >rmljhn77@gmail.com</NuxtLink
            >
          </h1>
          <h1 class="text-amber-300 font-bold w-[17.4rem]">
            Contact #:
            <span class="text-white">09472311383</span>
          </h1>
          <h1 class="text-amber-300 font-bold w-[17.4rem]">
            Address:
            <span class="text-white">
              Brgy 772, Raymundo Street, San Andres Bukid Manila</span
            >
          </h1>
        </div>
        <div class="flex flex-col w-1/2 justify-center space-y-6 p-6">
          <!-- Input for Name -->
          <input
            type="text"
            v-model="name"
            placeholder="Enter your name"
            class="border border-gray-300 rounded-md py-2 px-4 w-1/2"
          />

          <!-- Input for Message -->
          <textarea
            v-model="message"
            placeholder="Enter your message"
            class="border border-gray-300 rounded-md py-2 px-4 h-1/2 resize-none"
          ></textarea>
          <button class="text-black font-bold bg-amber-300 w-1/5 p-4 rounded-[2rem]">Send Message</button>
        </div>
      </div>
    </div>
  </div>
 </slot>
</template>
      
<script>
export default {
  data() {
    return {
      name: "",
      message: "",
    };
  },
};
</script>