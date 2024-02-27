<template>
  <slot>
  <div class="w-full bg-[#020617] h-20 flex flex-row fixed font-bold shadow-lg text-white">
    <div class="w-1/2 flex justify-start items-center flex-row">
      <NuxtLink to="/" @click="scrollToHome" class="flex items-center">
        <img src="~/assets/images/Rimel.png" alt="" class="h-[13rem] transition-transform transform hover:scale-110">
        <h1 class="text-[1.4rem] hover:text-amber-300">Rimel John</h1>
      </NuxtLink>
    </div>
    <div class="w-1/2 flex items-center px-8 justify-end space-x-8">
      <NuxtLink to="/" @click="scrollToHome" class="hover:text-amber-300">HOME</NuxtLink>
      <NuxtLink to="/about" @click="scrollToAbout" class="hover:text-amber-300">ABOUT ME</NuxtLink>
      <NuxtLink to="/services" @click="scrollToService" class="hover:text-amber-300">SERVICES</NuxtLink>
      <NuxtLink to="/project" @click="scrollToProject" class="hover:text-amber-300">PORTFOLIO</NuxtLink>
      <NuxtLink to="/contact" @click="scrollToContact" class="hover:text-amber-300">CONTACT</NuxtLink>
    </div>
  </div>
 </slot>
</template>

<script>
export default {
  methods: {
    scrollToContact() {
      // Scroll to the Services section when the link is clicked
      const contactSection = this.$parent.$refs.contactSection; // Check this line
      if (contactSection) {
        contactSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
    scrollToProject() {
      // Scroll to the Services section when the link is clicked
      const projectSection = this.$parent.$refs.projectSection; // Check this line
      if (projectSection) {
        projectSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
    scrollToService() {
      // Scroll to the Services section when the link is clicked
      const serviceSection = this.$parent.$refs.serviceSection; // Check this line
      if (serviceSection) {
        serviceSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
    scrollToAbout() {
      // Scroll to the About section when the link is clicked
      const aboutSection = this.$parent.$refs.aboutSection;
      if (aboutSection) {
        aboutSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
    scrollToHome() {
      // Scroll to the Home section when the link is clicked
      const homeSection = this.$parent.$refs.homeSection;
      if (homeSection) {
        homeSection.scrollIntoView({ behavior: 'smooth' });
      }
    }
  }
};
</script>
