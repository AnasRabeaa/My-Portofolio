<template>
  <div>
    <SectionsTitle :name="'About Me'" />
    <div name="AboutView" class="flex flex-wrap">
      <div class="w-full md:w-1/2 p-6">
        I’m Anas Rabea, front-end developer from Egypt, 6 October. with 1+ year 
        experience in building responsive website with HTML, CSS, SASS, JavaScript, Angular. 
        I have richexperience in web site design and building and customization. I try to
        keep up with security and best practices, and am always looking for new
        things to learn. I love to talk with you about our unique.
      </div>
      <div
        class="w-full md:w-1/2 p-6 relative before:line-gradiant-y flex flex-col"
      >
        <InfoModifer
          v-for="data in aboutInfo"
          :key="data.name"
          :info="data.info"
          :name="data.name"
          class="before:last:hidden first:pt-0"
        />
      </div>
    </div>
    <SectionsTitle :name="'My Services'" class="pt-0" />
    <div class="flex flex-wrap text-center">
      <div
        class="w-full p-6 relative md:w-1/2 even:before:line-gradiant-y last:w-full after:line-gradiant-x"
        v-for="service in myServices"
        :key="service.title"
      >
        <font-awesome-icon
          class="bg-primary w-10 h-10 p-4 rounded-full text-white"
          :icon="`fa-solid ${service.icon}`"
        />
        <p class="text-white text-2xl font-bold py-4">{{ service.title }}</p>
        <p>
          {{ service.description }}
        </p>
      </div>
    </div>
    <SectionsTitle :name="'Clients'" class="pt-12" />
    <div class="flex flex-wrap">
      <span
        class="w-1/2 p-6 relative grayscale transition-all duration-500 hover:grayscale-0 md:w-1/4 before:line-gradiant-y after:line-gradiant-x"
        v-for="client in clients"
        :key="client.link"
      >
        <img
          :src="'img/clientLogos/' + client.img"
          :alt="client.alt"
          class="m-auto w-5/6 h-full"
        />
      </span>
    </div>
  </div>
</template>
<script>
  import SectionsTitle from "@/components/SectionsTitle.vue";
  import InfoModifer from "../components/InfoModifer.vue";
  export default {
    components: { SectionsTitle, InfoModifer },
    data() {
      return {
        aboutInfo: [
          {
            name: "Phone",
            info: "+201024330450",
          },
          {
            name: "Email",
            info: "anas.rabea1000@gmail.com",
          },
          {
            name: "Freelance",
            info: "Available",
          },
          {
            name: "Address",
            info: "6 October, Egypt",
          },
        ],
        myServices: [
          {
            icon: "fa-code",
            title: "Web Development",
            description:
              "Modern and mobile-ready website that will help you reach all of your marketing.",
          },
          {
            icon: "fa-mobile-screen-button",
            title: "Single Page Application ",
            description:
              "Creative Application fit in all operating systems to improve your bussnius.",
          },
          {
            icon: "fa-magnifying-glass-location",
            title: "Digital Marketing",
            description:
              "Advertising services include social media, SEO, and web apps.",
          },
        ],
        clients: [
          {
            img: "shukran-yasta.png",
            alt: "Shukran Yasta",
          },
          {
            img: "viganella.png",
            alt: "Viganella",
          },
          {
            img: "cav.svg",
            alt: "CAV",
          },
          {
            img: "bond.png",
            alt: "BOND",
          },
        ],
      };
    },
  };
</script>
