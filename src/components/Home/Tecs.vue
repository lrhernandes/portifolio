<template>
  <h2 class="text-[#272937] text-3xl text-center pb-6 pt-28">
    TECNOLOGIAS
  </h2>
  <p class="text-center text-gray-500 font-light text-md mb-11 px-4">
    Tecnologias de desenvolvimento que uso para desenvolvimento web e mobile
  </p>
  <article class="px-9 pt-20 pb-8 lg:px-36">
    <div class="mx-auto container">
      <Carousel :itemsToShow="1" :breakpoints="breakpoints">
        <Slide v-for="tec in tecs" :key="tec.name">
          <div class="tec-item">
            <img :src="tec.src" :alt="tec.name" />
            <h6 class="text-white pt-4">{{ tec.name }}</h6>
          </div>
        </Slide>

        <template #addons>
          <Navigation />
          <Pagination />
        </template>
      </Carousel>
    </div>
  </article>
</template>

<script>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
import { reactive } from "@vue/reactivity";
import { toRefs } from "vue";

import sass from "../../assets/tecs/sass.png";
import html from "../../assets/tecs/html.png";
import vue from "../../assets/tecs/vue.png";
import rn from "../../assets/tecs/react-native.png";
import css from "../../assets/tecs/css.png";
import react from "../../assets/tecs/react.png";
import js from "../../assets/tecs/js.png";
import node from "../../assets/tecs/node.png";
import mysql from "../../assets/tecs/mysql.png";
import bootstrap from "../../assets/tecs/bootstrap.png";
import figma from "../../assets/tecs/figma.svg";
import tailwind from "../../assets/tecs/tailwind.png";

export default {
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  setup() {
    const data = reactive({
      tecs: [
        { name: "SCSS", src: sass },
        { name: "HTML 5", src: html },
        { name: "Vue.js", src: vue },
        { name: "React Native", src: rn },
        { name: "CSS", src: css },
        { name: "React", src: react },
        { name: "Javascript", src: js },
        { name: "Node", src: node },
        { name: "MySQL", src: mysql },
        { name: "Bootstrap", src: bootstrap },
        { name: "Figma", src: figma },
        { name: "Tailwind CSS", src: tailwind },
      ],
      breakpoints: {
        450: {
          itemsToShow: 2,
          snapAlign: "center",
        },
        600: {
          itemsToShow: 3,
          snapAlign: "center",
        },
        700: {
          itemsToShow: 4,
          snapAlign: "center",
        },
        // 1024 and up
        1324: {
          itemsToShow: 5,
          snapAlign: "center",
        },
        1500: {
          itemsToShow: 6,
          snapAlign: "center",
        },
      },
    });

    return { ...toRefs(data) };
  },
};
</script>

<style scoped>
article {
  background-image: url("../../assets/bar.png");
  background-size: cover;
  background-repeat: round;
}

.tec-item {
  transition: all 0.5s;
  filter: gray; /* IE6-9 */
  -webkit-filter: grayscale(1); /* Google Chrome, Safari 6+ & Opera 15+ */
  filter: grayscale(1); /* Microsoft Edge and Firefox 35+ */
}
.tec-item img {
  height: 110px;
  width: 120px;
  min-width: 120px;
}

@media screen and (min-width: 1000px) {
  .tec-item img {
    height: 150px;
    width: 150px;
    min-width: 150px;
  }
}

.tec-item:hover {
  filter: none;
}

.tec-item h6 {
  color: #272937;
  transition: all 0.5s;
}

.tec-item:hover h6 {
  color: white;
}

.carousel__item {
  min-height: 200px;
  width: 100%;
  background-color: var(--vc-clr-primary);
  color: var(--vc-clr-white);
  font-size: 20px;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}
</style>
