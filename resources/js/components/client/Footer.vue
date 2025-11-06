<template>
  <footer class="bg-[#F6EED0] text-[#3A2A13] py-8 font-sans">
    <div class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-4 gap-6">
      <!-- Cột 1: Logo + thông tin liên hệ -->
      <div class="flex flex-col gap-4">
        <img
          src="/images/homepage/logo-coffee.png"
          alt="Ông Quan Coffee"
          class="w-30 h-30 object-contain"
        />
        <div class="flex items-center">
          <div>
            <h3 class="font-holiday text-lg font-bold uppercase text-[#3A2A13] my-4">
              Tiệm cà phê Ông Quan
            </h3>
            <p class="text-sm leading-relaxed text-[#3A2A13]/80">
              Địa chỉ: hẻm 583, đường 30/4, phường Hưng Lợi, quận Ninh Kiều, TP.
              Cần Thơ, Việt Nam <br />
              Điện thoại: 093 729 65 65
            </p>
          </div>
        </div>

        <!-- Mạng xã hội -->
        <div class="flex items-center gap-4 mt-2">
          <a href="#" aria-label="Facebook">
            <img
              src="/images/homepage/fb.png"
              alt="Facebook"
              class="w-6 h-6 hover:opacity-80 transition"
            />
          </a>
          <a href="#" aria-label="Instagram">
            <img
              src="/images/homepage/ig.png"
              alt="Instagram"
              class="w-6 h-6 hover:opacity-80 transition"
            />
          </a>
          <a href="#" aria-label="YouTube">
            <img
              src="/images/homepage/ytb.png"
              alt="YouTube"
              class="w-6 h-6 hover:opacity-80 transition"
            />
          </a>
          <a href="#" aria-label="Twitter">
            <img
              src="/images/homepage/twitter.png"
              alt="Twitter"
              class="w-6 h-6 hover:opacity-80 transition"
            />
          </a>
        </div>
      </div>

      <!-- Cột 2: Giới thiệu -->
      <div class="md:pl-18 mt-4">
        <h4 class="font-oswald text-xl text-[#3A2A13] font-bold uppercase mb-3">Giới thiệu</h4>
        <ul class="space-y-2 text-sm text-[#3A2A13]/80">
          <li><a href="#" class="hover:text-black">Về chúng tôi</a></li>
          <li><a href="#" class="hover:text-black">Ưu đãi</a></li>
        </ul>
      </div>

      <!-- Cột 3: Dịch vụ khách hàng -->
      <div class="md:pl-18 mt-4">
        <h4 class="font-oswald text-xl text-[#3A2A13] font-bold uppercase mb-3">
          Dịch vụ khách hàng
        </h4>
        <ul class="space-y-2 text-sm text-[#3A2A13]/80">
          <li><a href="#" class="hover:text-black">Liên hệ</a></li>
          <li><a href="#" class="hover:text-black">Hỗ trợ khách hàng</a></li>
        </ul>
      </div>

      <!-- Cột 4: Điều khoản -->
      <div class="md:pl-18 mt-4">
        <h4 class="font-oswald text-xl text-[#3A2A13] font-bold uppercase mb-3">Điều khoản</h4>
        <ul class="space-y-2 text-sm text-[#3A2A13]/80">
          <li><a href="#" class="hover:text-black">Điều khoản sử dụng</a></li>
          <li>
            <a href="#" class="hover:text-black"
              >Chính sách bảo mật thông tin</a
            >
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script setup>
// Không cần script phức tạp ở đây
</script>

<style scoped>
footer {
  font-family: "Inter", sans-serif;
}
</style>
