<template>
  <h2 class="text-[#272937] font-major text-3xl">TECNOLOGIAS</h2>
  <Carousel :items-to-show="1.5">
    <Slide v-for="tec in tecs" :key="tec.name">
      {{ tec }}
    </Slide>

    <template #addons>
      <Navigation />
      <Pagination />
    </template>
  </Carousel>
</template>

<script>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
import { reactive } from "@vue/reactivity";
import { toRefs } from "vue";
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
        { name: "SCSS", src: "../../assets/tecs/sass.png" },
        { name: "HTML 5", src: "../../assets/tecs/html.png" },
        { name: "Vue.js", src: "../../assets/tecs/vue.png" },
        { name: "React Native", src: "../../assets/tecs/react-native.png" },
        { name: "CSS", src: "../../assets/tecs/css.png" },
        { name: "React", src: "../../assets/tecs/react.png" },
        { name: "Javascript", src: "../../assets/tecs/js.png" },
        { name: "Node", src: "../../assets/tecs/node.png" },
        { name: "MySQL", src: "../../assets/tecs/mysql.png" },
        { name: "Bootstrap", src: "../../assets/tecs/bootstrap.png" },
        { name: "Figma", src: "../../assets/tecs/figma.svg" },
        { name: "Tailwind CSS", src: "../../assets/tecs/tailwind.png" },
      ],
    });

    return { ...toRefs(data) };
  },
};
</script>

<style scoped>

.carousel__item {
  min-height: 200px;
  width: 100%;
  background-color: var(--vc-clr-primary);
  color:  var(--vc-clr-white);
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
