<template>
  <div class="space-y-6">
    <NuxtImg
      src="/avatar.png"
      alt="Fayaz Ahmed"
      class="ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 bg-gray-200 dark:bg-gray-900 rounded-full h-12 w-12 sm:h-16 sm:w-16"
      sizes="48px sm:64px"
      placeholder
      format="webp"
    />
    <!-- weixindushu rutuweian nicainnegxingfu jiqihaoixangzaimengli  daizhe yixiang  -->

    <h1
      class="text-xl font-bold tracking-tight text-gray-800 dark:text-gray-100"
    >
      Hello!
    </h1>
    <p class="text-gray-900 dark:text-gray-200">
      程序员一枚，擅长使用Javascript, React, Vue和Node构建web应用程序和网站。
    </p>
    <p ref="greetRef" class="text-gray-600 dark:text-gray-500"></p>
  </div>
</template>

<script setup>
import Typed from "typed.js";
import { onMounted, onUnmounted, ref } from "vue";
const greetRef = ref(null);
const typed = ref(null);
onMounted(() => {
  typed.value = new Typed(greetRef.value, {
    strings: ["在数字的森林里，作探险的旅者，用键盘解锁谜题，用屏幕展现世界。"],
    typeSpeed: 50,
    backSpeed: 30,
    // showCursor: false,
  });
});
onUnmounted(() => typed.value.destroy());
useSeoMeta({
  title: "Jon Hao",
  description:
    "I specialize in building web applications and sites using Javascript, React, Vue & Node.",
});
</script>
