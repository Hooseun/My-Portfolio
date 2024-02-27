<template>
  <slot>
    <div class="h-[55.6rem] bg-[#020617] flex items-center justify-center">
      <div class="w-5/6 h-5/6 flex flex-col items-center">
        <h1 class="text-[4rem] font-bold text-white">
          MY <span class="text-amber-300"> PORTFOLIO</span>
        </h1>
        <p class="text-center mt-8 w-[30rem] text-[#6B7280]">This is my Sample Projects that I worked on! Feel free to View it!</p>
        <div class="grid grid-cols-4 gap-4 mt-[4rem] w-full space-x-9">
          <div v-for="project in displayedProjects" :key="project.id" class="bg-gray-300 text-center p-1 rounded-xl h-[30rem] relative">
            <img :src="project.imageUrl" alt="Project Image" class="w-[30rem] h-[14rem] object-cover rounded-xl">
            <h2 class="px-7 text-xl font-bold mt-4 text-start">{{ project.title }}</h2>
            <p class="ml-4 mt-4 flex items-start">
              <span class="px-2 ">
                <span v-for="lang in project.languages" :key="lang" class="inline-block bg-blue-500 text-white rounded-full px-2 py-1 text-sm font-semibold mr-2">{{ lang }}</span>
              </span>
            </p>
            <p class="px-7 mt-2 text-start text-[11px]">{{ project.description }}</p>
          </div>
        </div>
        <div class="mt-[3rem] space-x-4 flex flex-row">
          <button @click="previousPage" :disabled="currentPage === 1" class="text-white"> << </button>
          <div>
            <button v-for="page in totalPages" :key="page" @click="currentPage = page" :class="{ 'text-yellow-500': currentPage === page }" class="text-white px-1">{{ page }}</button>
          </div>
          <button @click="nextPage" :disabled="currentPage === totalPages" class="text-white">>></button>
        </div>
      </div>
    </div>
  </slot>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { 
          id: 1, 
          title: 'MARAHUYO', 
          imageUrl: 'Marahuyo.png', 
          languages: ['ReactJS', 'MySQL'], 
          description: 'Marahuyo is an E-commerce website for Organizations in TUP-Manila for the students to buy and sell the merchandises of their organizations' 
        },
        { 
          id: 2, 
          title: 'BARANGAY E-SERVICES MANAGEMENT', 
          imageUrl: 'BEMS.png', 
          languages: ['ReactJs', 'MongoDB'],
          description: 'The "Barangay E-Services Management: Web and Android Application” is an application that aims to provide centralized platform for the citizens of Municipality of Rodriguez, Rizal that automates the process of managing various services from residents of different barangays in the community through Web, and Android application.' 
        },
        { 
          id: 3, 
          title: 'EZ COIN Laundry', 
          imageUrl: 'EZ COIN.png', 
          languages: ['PHP', 'MySQL'], 
          description: 'A Payroll management system for laundry shops to make the payment of laundry shop much easier and easy access for clients.' 
        },
        { 
          id: 4, 
          title: 'GENERIC SERVICE REQUEST MANAGEMENT', 
          imageUrl: 'GSRM.png', 
          languages: ['ReactJS', 'MySQL'], 
          description: 'A Service Request Management for Technological University of the Phillipines Students for them to access easier and request services more easier.' 
        },
        { 
          id: 5, 
          title: 'Portfolio', 
          imageUrl: 'Portfolio.png', 
          languages: ['ReactJS', 'MongoDB'], 
          description: 'This is my other portfolio that i have been deployed' 
        },
        { 
          id: 6, 
          title: 'VAXX RECORD SYSTEM', 
          imageUrl: 'VaxxRecord.png', 
          languages: ['Ruby'], 
          description: 'This is a console based system that tracks the record of the people who has been vaccinated' 
        },
        { 
          id: 7, 
          title: 'KAKOS', 
          imageUrl: 'kakos.png', 
          languages: ['Framer'], 
          description: 'Online website development that is accessible for customers and resellers alike providing them design, development, sourcing, manufacturing and retail.' 
        },
        { 
          id: 8, 
          title: 'Coffee Articles', 
          imageUrl: 'Joomla.png', 
          languages: ['Joomla', 'WAMP'], 
          description: 'Website to browse and see a different type of Coffee and other coffee businesses' 
        },
      ],
      itemsPerPage: 4,
      currentPage: 1,
    };
  },
  computed: {
    totalPages() {
      return Math.ceil(this.items.length / this.itemsPerPage);
    },
    displayedProjects() {
      const start = (this.currentPage - 1) * this.itemsPerPage;
      const end = start + this.itemsPerPage;
      return this.items.slice(start, end);
    }
  },
  methods: {
    nextPage() {
      if (this.currentPage < this.totalPages) {
        this.currentPage++;
      }
    },
    previousPage() {
      if (this.currentPage > 1) {
        this.currentPage--;
      }
    }
  }
};
</script>
