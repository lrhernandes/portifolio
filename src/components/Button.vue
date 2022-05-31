<template>
    <div :class="light? 'text-[#272937] bg-white w-max font-medium px-5 py-2 rounded-md uppercase' : 'text-white bg-[#272937] w-max font-medium px-5 py-2 rounded-md uppercase'">
        {{text}}
    </div>
</template>
<script>
export default {
  props: { text: String, light: Boolean, dark: Boolean },
  setup() {
    //   return {text, light, dark}
  },
};
</script>
