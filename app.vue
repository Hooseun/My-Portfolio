<template>
  <div>
    <Navbar />
    <Section ref="homeSection">
      <Home />
    </Section>
    <Section ref="aboutSection">
      <About />
    </Section>
    <Section ref="serviceSection">
      <Services />
    </Section>
    <Section ref="projectSection">
      <Project />
    </Section>
    <Section ref="contactSection">
      <Contact />
    </Section>
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
import About from "~/components/About.vue";
import Home from "~/components/Home.vue";
import Services from "~/components/Services.vue";
import Project from "~/components/Project.vue"
import Contact from "~/components/Contact.vue"

export default {
  components: {
    Navbar,
    About,
    Home,
    Services,
    Project,
    Contact
  },
};
</script>
