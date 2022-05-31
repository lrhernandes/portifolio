<template>
  <section class="w-full bg-[#272937]">
    <div class="noise-mask">
      <div class="container flex flex-row justify-around items-center mx-auto">
        <div class="py-40 mr-16">
          <h1 class="text-white text-4xl py-10 font-major">
            Desenvolvedora frontend
          </h1>
          <Button text="Entrar em contato" light />
        </div>
        <div class="relative w-64 lg:w-80 py-48">
          <img class="" src="../../assets/Ellipse 2.png" alt="Perfil" />
          <!-- <div>
        <img
          class="absolute z-20"
          src="../../assets/Ellipse 4.svg"
          alt="Elipse linha"
        />
        <img
          class="absolute z-20"
          src="../../assets/Ellipse 3.svg"
          alt="Elipse preenchida"
        />
        <img
          class="absolute z-20"
          src="../../assets/Star 1.svg"
          alt="Estrela"
        />
      </div> -->
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Button from "../Button.vue";
export default {
  components: { Button },
  setup() {},
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Major+Mono+Display&display=swap");
h1 {
  font-family: "Major Mono Display", monospace;
}
.noise-mask {
  background-image: url("../../assets/noise.png");
  background-repeat: repeat;
}
</style>
