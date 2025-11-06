<template>
  <!-- Navbar Desktop -->
  <section
    class="relative z-100 h-20 items-center justify-end xl:justify-center hidden xl:flex bg-[#594633]"
  >
    <!-- Logo -->
    <img
      class="cursor-pointer absolute left-[10%] z-100 w-auto h-18"
      src="/images/homepage/logo-coffee.png"
      alt="logo"
    />

    <!-- Menu Desktop -->
    <ul class="font-oswald flex items-center z-100 relative">
      <li
        v-for="(item, index) in navbarItem"
        :key="index"
        class="uppercase font-bold text-base transition-colors duration-200"
        :class="
          item.active ? 'text-[#F1E8C7]' : 'text-[#F1E8C7] hover:text-white'
        "
      >
        <a class="px-10 py-4" :href="item.href">{{ item.name }}</a>
      </li>
    </ul>

    <div class="flex items-center">
      <SearchIcon
        class="w-6 h-6 ml-10 text-[#F1E8C7] hover:text-white cursor-pointer"
      />
    </div>
  </section>

  <!-- Navbar Mobile -->
  <section
    class="relative z-100 h-20 flex items-center justify-center px-6 xl:hidden bg-[#594633]"
  >
    <!-- Logo cho Tablet -->
    <img
      class="absolute max-md:hidden top-1/3 left-[10%] z-100"
      src="/images/homepage/logo-coffee.png"
      alt="logo"
    />

    <!-- Logo Mobile -->
    <img
      class="z-100 h-14 object-contain"
      src="/images/homepage/logo-coffee.png"
      alt="mobile_logo"
    />

    <!-- Nút mở menu -->
    <button
      v-if="!isOpen"
      @click="isOpen = true"
      class="absolute z-101 right-6 text-[#F1E8C7] hover:text-white"
    >
      <MenuIcon class="w-7 h-7" />
    </button>

    <!-- Overlay (mờ nền khi menu mở) -->
    <transition name="fade">
      <div
        v-if="isOpen"
        class="fixed inset-0 bg-black/40 z-90"
        @click="isOpen = false"
      ></div>
    </transition>

    <!-- Menu trượt -->
    <transition name="slide">
      <div
        v-if="isOpen"
        class="fixed top-0 right-0 h-full bg-white shadow-lg z-100 p-6 w-[80%] max-w-[400px] min-[360px]:w-full transition-transform"
      >
        <div class="flex justify-end mb-6">
          <button
            @click="isOpen = false"
            class="text-gray-500 hover:text-[#880000B8] text-2xl"
          >
            &times;
          </button>
        </div>

        <!-- Danh sách menu Mobile -->
        <ul class="flex flex-col gap-3">
          <li
            v-for="(item, index) in navbarItem"
            :key="index"
            class="border-b border-gray-100 pb-2"
          >
            <a
              :href="item.href"
              class="block text-lg font-semibold text-gray-700 hover:text-[#880000B8]"
              @click="isOpen = false"
            >
              {{ item.name }}
            </a>
          </li>
        </ul>
      </div>
    </transition>
  </section>
</template>

<script setup>
import { ref } from "vue";

const isOpen = ref(false);

const navbarItem = [
  { name: "Trang Chủ", href: "#", active: true },
  { name: "Thực Đơn", href: "#", active: false },
  { name: "Ưu Đãi", href: "#", active: false },
  { name: "Về Chúng Tôi", href: "#", active: false },
  { name: "Liên Hệ", href: "#", active: false },
];
</script>

<style scoped>
/* Hiệu ứng fade overlay */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

/* Hiệu ứng slide menu mobile */
.slide-enter-active,
.slide-leave-active {
  transition: transform 0.2s ease;
}
.slide-enter-from {
  transform: translateX(100%);
}
.slide-leave-to {
  transform: translateX(100%);
}
</style>
