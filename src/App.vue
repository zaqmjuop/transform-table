<template>
  <div id="app">
    <div>
      <label v-for="(item, index) in EXAMPLES" :key="index">
        <span> Example{{ index + 1 }}</span>
        <input
          type="radio"
          name="exampleTarget"
          :value="index"
          :checked="exampleTarget === index"
          @input="exampleTarget = index"
      /></label>
    </div>
    <div>
      <component :is="EXAMPLES[exampleTarget]"></component>
    </div>
  </div>
</template>

<script setup lang="ts">
import Vue, { ref } from "vue";
import Example1 from "@/components/Example1.vue";
import Example2 from "@/components/Example2.vue";
import Example3 from "@/components/Example3.vue";
import Example4 from "@/components/Example4.vue";
import Example5 from "@/components/Example5.vue";
import Example6 from "@/components/Example6.vue";
import Example7 from "@/components/Example7.vue";
const EXAMPLES = [
  Example1,
  Example2,
  Example3,
  Example4,
  Example5,
  Example6,
  Example7,
];
const exampleTarget = ref(0);
</script>

<style scoped></style>
