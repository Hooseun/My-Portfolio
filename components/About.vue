<template>
  <slot>
  <div class="h-[55.6rem] bg-[#020617] flex flex-row">
    <div class="h-[55.6rem] w-1/2 flex justify-center items-center">
      <div class=" px-10 py-5 relative">
        <div class="rounded-xl absolute border-[1.5rem]  border-amber-400 h-[40rem] w-[35.6rem] mt-12 right-[5.5rem]"></div>
        <img src="~/assets/images/Batallones.jpg" alt="" class="rounded-xl h-[40rem] relative z-10" />
      </div>
    </div>
    <div class="w-1/2" ref="aboutSection">
      <div class="w-full h-full flex justify-center items-center flex-col">
        <div class="w-full h-1/2 p-2 ">
          <!-- Add a ref attribute to the section -->
          <h1  class="text-[3rem] font-bold text-white">ABOUT <span class="text-amber-300">ME</span></h1>
          <p  class="mt-10 text-[1.2rem] text-[#6B7280] w-5/6">Hello! I'm Rimel John Batallones, a passionate BSIT Student with a keen eye for Web Developing. I thrive on creativity and enjoy crafting unique solutions to complex problems. With a background in Information Technology, I bring a blend of technical expertise and creative thinking to every project I undertake.</p>
          <p  class="mt-10 text-[1.2rem] text-[#6B7280] w-5/6">In addition to my technical skills, I'm a firm believer in collaboration and effective communication. I enjoy working closely with clients and team members to understand their needs and deliver solutions that exceed expectations.

            When I'm not coding or designing, you can find me Online Gaming. I believe in maintaining a healthy work-life balance to stay inspired and creative.</p>
          <!-- Bind mouseover and mouseleave events for hover effect -->
          <button @mouseover="hoverEffect" @mouseleave="resetEffect" @click="clickAnimation" class="mt-10 text-black bg-amber-400 text-xl p-4 rounded-[2rem] font-bold">
            Contact me
          </button>
        </div>
      </div>
    </div>
  </div>
</slot>
</template>

<script>
export default {
 
  methods: {
    // Method to handle hover effect
    hoverEffect(event) {
      event.target.style.transform = 'scale(1.1)';
      event.target.style.transition = 'transform 0.3s ease';
    },
    // Method to reset hover effect
    resetEffect(event) {
      event.target.style.transform = 'scale(1)';
    },
    // Method to handle click animation
    clickAnimation(event) {
      event.target.style.transform = 'scale(0.9)';
      setTimeout(() => {
        event.target.style.transform = 'scale(1)';
      }, 200); // Adjust the time as needed for the animation duration
      // Scroll to the Contact section
      this.scrollToContact();
    },
    // Method to scroll to the Contact section
    scrollToContact() {
      const contactSection = this.$parent.$refs.contactSection;
      if (contactSection) {
        contactSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
  },
};
</script>

<style scoped>
/* Add slide-in animation styles */
.slide-in-right {
  animation: slideInRight 1s ease forwards;
}

@keyframes slideInRight {
  from {
    transform: translateX(100%);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}
</style>
