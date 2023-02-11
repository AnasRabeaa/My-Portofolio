<template>
  <div>
    <SectionsTitle :name="'Recent Works'" />
    <div
      class="relative before:hidden md:before:block before:line-gradiant-y before:left-1/2"
    >
      <WorksCard
        class="w-full md:w-1/2 inline-block"
        v-for="work in works"
        :key="work.title"
        :title="work.title"
        :img="work.img"
        :modalImg="work.modalImg"
      />
    </div>
  </div>
</template>

<script>
  import SectionsTitle from "@/components/SectionsTitle.vue";
  import WorksCard from "@/components/WorksCard.vue";
  export default {
    components: { SectionsTitle, WorksCard },
    data() {
      return {
        works: [
          {
            title: "Bella Mart",
            img: "img/works/bella-mart.jpg",
            modalImg: "img/works/bella-mart.jpg",
          },
          {
            title: "Alaa Elden",
            img: "img/works/alaaedint.jpg",
            modalImg: "img/works/alaaedint.jpg",
          },
          {
            title: "Egy Golf",
            img: "img/works/golf.jpg",
            modalImg: "img/works/golf.jpg",
          },
          {
            title: "Digital Bond",
            img: "img/works/bondform.jpg",
            modalImg: "img/works/bondform.jpg",
          },
          {
            title: "Portofolio",
            img: "img/works/portofolio.jpg",
            modalImg: "img/works/portofolio.jpg",
          },
          {
            title: "Bandi",
            img: "img/works/Preview.png",
            modalImg: "img/works/Preview.png",
          },
          {
            title: "Food Restaurant",
            img: "img/works/resto.jpg",
            modalImg: "img/works/resto.jpg",
          },
          {
            title: "E-commerce",
            img: "img/works/e-commerce.jpg",
            modalImg: "img/works/e-commerce.jpg",
          },
          {
            title: "Memory Game",
            img: "img/works/game.jpg",
            modalImg: "img/works/game.jpg",
          },
          {
            title: "Anas Rabea",
            img: "img/works/anas.jpg",
            modalImg: "img/works/anas.jpg",
          },
        ],
      };
    },
  };
</script>
