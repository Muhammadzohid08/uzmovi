<script setup>
import { ref, onMounted } from "vue";

const kinolarType = ref(null);
const kinoCategory = ref(null);

onMounted(() => {
  if (kinolarType.value && kinoCategory.value) {
    kinolarType.value.addEventListener("click", () => {
      kinoCategory.value.classList.add("flex");
      console.log('ishladi');
    });
  }
});
</script>

<template>
  <div
    class="w-full h-[105px] flex justify-center items-center bg-[#222933] px-2"
  >
    <div class="container w-[77%] flex justify-between items-center relative">
      <img src="../../public/logo.gif" alt="" />
      <div class="w-full h-[105px] flex justify-center items-center ml-28">
        <div
          style="transition: 0.5s all ease"
          class="cursor-pointer w-auto px-2 border-b-[4px] border-[#7F4726] h-full flex justify-center items-center hover:bg-[#7F4726]"
        >
          <h2 class="uppercase text-[#99BBDC] text-[15px]">Boshqa Sahifa</h2>
        </div>
        <div
          style="transition: 0.5s all ease"
          ref="kinolar-type"
          class="cursor-pointer w-auto px-2 h-full flex justify-center border-b-[4px] border-[#2A6C4E] items-center hover:bg-[#2A6C4E]"
        >
          <h2 class="uppercase text-[#99BBDC] text-[15px]">
            kinolar <i class="fa-solid fa-caret-down ml-2"></i>
          </h2>
        </div>
        <div
          style="transition: 0.5s all ease"
          class="cursor-pointer w-auto px-2 h-full flex justify-center border-b-[4px] border-[#1A637E] items-center hover:bg-[#1A637E]"
        >
          <h2 class="uppercase text-[#99BBDC] text-[15px]">seriallar</h2>
        </div>
        <div
          style="transition: 0.5s all ease"
          class="cursor-pointer w-auto px-2 h-full flex justify-center border-b-[4px] border-[#7E273C] items-center hover:bg-[#7E273C]"
        >
          <h2 class="uppercase text-[#99BBDC] text-[15px]">
            janr <i class="fa-solid fa-caret-down ml-1"></i>
          </h2>
        </div>
        <div
          style="transition: 0.5s all ease"
          class="cursor-pointer w-auto px-2 h-full flex justify-center border-b-[4px] border-[#7F6A3F] items-center hover:bg-[#7F6A3F]"
        >
          <h2 class="uppercase text-[#99BBDC] text-[15px]">
            yil <i class="fa-solid fa-caret-down ml-1"></i>
          </h2>
        </div>
        <div
          style="transition: 0.5s all ease"
          class="cursor-pointer w-auto px-2 h-full flex justify-center border-b-[4px] border-[#553E6A] items-center hover:bg-[#553E6A]"
        >
          <h2 class="uppercase text-[#99BBDC] text-[15px]">
            mamlakat <i class="fa-solid fa-caret-down ml-1"></i>
          </h2>
        </div>
        <div
          style="transition: 0.5s all ease"
          class="cursor-pointer w-auto px-2 h-full flex justify-center border-b-[4px] border-[#ff690766] items-center hover:bg-[#ff690766]"
        >
          <h2 class="uppercase text-[#99BBDC] text-[15px]">
            kino yangiliklari
          </h2>
        </div>
      </div>
      <div
        ref="kino-category"
        class="w-full h-[100px] absolute bg-[#232F3D] top-[120px] rounded-[5px] justify-center items-center px-5 gap-2 hidden"
      >
        <h1
          class="cursor-pointer w-full py-2 flex justify-center items-center text-[#8FB1D4] bg-[#304156] text-[15px] rounded-[5px]"
        >
          Tarjima kinolar
        </h1>
        <h1
          class="cursor-pointer w-full py-2 flex justify-center items-center text-[#8FB1D4] bg-[#304156] text-[15px] rounded-[5px]"
        >
          Premyeralar
        </h1>
        <h1
          class="cursor-pointer w-full py-2 flex justify-center items-center text-[#8FB1D4] bg-[#304156] text-[15px] rounded-[5px]"
        >
          Hind kinolar
        </h1>
        <h1
          class="cursor-pointer w-full py-2 flex justify-center items-center text-[#8FB1D4] bg-[#304156] text-[15px] rounded-[5px]"
        >
          Multfilm
        </h1>
        <h1
          class="cursor-pointer w-full py-2 flex justify-center items-center text-[#8FB1D4] bg-[#304156] text-[15px] rounded-[5px]"
        >
          Kino yangiliklari
        </h1>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>