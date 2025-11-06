<template class="font-banque">
  <!-- Navbar component -->
  <Navbar />

  <section
    class="relative flex justify-center items-center w-full h-80 md:h-[520px] lg:h-[720px] bg-[url('/images/homepage/bg-homepage.png')] bg-cover bg-center"
  >
    <!-- Lớp phủ mờ -->
    <div class="absolute inset-0 bg-[#000000]/40"></div>

    <!-- Nội dung -->
    <div class="relative z-10 text-center flex flex-col items-center px-4">
      <!-- Tiêu đề chính -->
      <h1
        class="font-yeseva-one uppercase text-[#F8F5E7] text-[33px] md:text-[56px] lg:text-[72px] leading-[1.1] tracking-[1px] drop-shadow-[0_2px_4px_rgba(0,0,0,0.5)]"
      >
        Tiệm cà phê Ông Quan
      </h1>

      <!-- Tagline -->
      <p
        class="font-playfair text-[#EADFC5] text-[14px] md:text-[18px] lg:text-[20px] italic mt-3 mb-5"
      >
        Không chỉ là coffee, chúng tôi bán với sự trải nghiệm
      </p>

      <!-- Nút hành động -->
      <a
        href="#"
        class="uppercase font-bold text-[#3A2A13] bg-[#F1E8C7] hover:bg-[#F8F5E7] shadow-md px-6 py-2 text-[13px] md:text-[15px] transition-all duration-300"
      >
        Đặt hàng
      </a>
    </div>
  </section>

  <section class="bg-[#F6EED0] py-16 md:py-14 px-6 text-center font-playfair">
    <!-- Tiêu đề -->
    <div class="max-w-4xl mx-auto mb-12">
      <p
        class="uppercase text-[#6B5638] tracking-[2px] text-sm md:text-base mb-6"
      >
        Trải nghiệm
      </p>
      <h2
        class="font-anton text-3xl md:text-5xl text-[#594633] font-extrabold uppercase mb-8"
      >
        Về Không Gian
      </h2>
      <p
        class="text-[#594633]/80 text-[14px] md:text-[16px] leading-relaxed font-prata"
      >
        Tiệm Cà Phê Ông Quan là một ẩn mình trong lòng Cần Thơ, mang đến cho bạn
        một trải nghiệm độc đáo với không gian lấy cảm hứng từ vẻ đẹp của Đà
        Lạt. Với tông màu ấm áp và thoải mái, chúng tôi đã thiết kế do nội thất
        thông minh và tinh tế để tạo ra một môi trường đặc biệt, mang đến sự
        thoải mái tối đa cho khách hàng. Bạn có thể lựa chọn ngồi ở các góc
        riêng tư, hoặc tận hưởng không gian mở tùy theo sở thích của mình. Chúng
        tôi luôn sẵn sàng đón tiếp và mang đến cho bạn cảm giác thư giãn, hòa
        mình vào vẻ đẹp mộc mạc của Đà Lạt ngay tại Cần Thơ.
      </p>
    </div>

    <!-- Hình ảnh -->
    <div class="block md:hidden">
      <swiper
        :modules="[Pagination]"
        :slides-per-view="1"
        :space-between="20"
        :pagination="{ clickable: true }"
        class="mySwiper"
      >
        <swiper-slide v-for="(img, i) in images" :key="i">
          <img
            :src="img.src"
            :alt="img.alt"
            class="w-full h-[350px] object-cover rounded-md shadow-md"
          />
        </swiper-slide>
      </swiper>
    </div>

    <!-- Desktop: 3 ảnh grid -->
    <div class="hidden md:grid max-w-7xl mx-auto grid-cols-3 gap-8">
      <div
        v-for="(img, i) in images"
        :key="i"
        class="cursor-pointer overflow-hidden rounded-md shadow-md hover:shadow-xl transition-all duration-300"
      >
        <img
          :src="img.src"
          :alt="img.alt"
          class="w-full h-full object-cover hover:scale-105 transition-transform duration-500"
        />
      </div>
    </div>
  </section>

  <section
    class="relative flex flex-col items-center justify-center bg-[#594633] text-center py-5 md:py-10 overflow-hidden"
  >
    <!-- Ly cà phê -->
    <img
      src="/images/homepage/best-seller.png"
      alt="Cà phê sữa Ông Quan"
      class="relative z-10 w-[280px] md:w-[300px] object-contain top-10"
    />
    <div class="absolute inset-0 bg-black/35 z-10"></div>

    <!-- Text chồng lên giữa -->
    <div
      class="absolute inset-0 flex flex-col items-center justify-center text-[#F1E8C7] z-20 px-6"
    >
      <h3
        class="font-anton text-[42px] md:text-[68px] lg:text-[80px] uppercase tracking-wider mb-2 drop-shadow-[0_2px_4px_rgba(0,0,0,0.5)]"
      >
        Best Seller #1
      </h3>
      <p
        class="font-smooch font-bold text-[18px] md:text-[40px] uppercase mb-6 tracking-[1px]"
      >
        Cà Phê Sữa
      </p>

      <a
        href="#"
        class="uppercase text-[#3A2A13] px-6 py-2 font-bold text-[13px] md:text-[15px] shadow-md bg-[#F1E8C7] hover:bg-[#F8F5E7] transition-all duration-300"
      >
        Tìm hiểu thêm
      </a>
    </div>

    <!-- Hiệu ứng gradient nền -->
    <div
      class="absolute inset-0 bg-linear-to-b from-[#594633]/80 via-[#594633]/90 to-[#3A2A13]/95"
    ></div>
  </section>

  <section class="bg-[#F6EED0] py-16 md:py-24 px-6 font-playfair text-center">
    <!-- Tiêu đề chính -->
    <div class="max-w-5xl mx-auto mb-12">
      <h2 class="text-[#3A2A13] text-3xl md:text-5xl font-anton uppercase mb-8">
        Thực đơn có gì?
      </h2>

      <!-- Tabs -->
      <div
        class="flex justify-center gap-8 text-[#3A2A13]/60 font-smooch font-bold text-lg md:text-xl uppercase mb-10"
      >
        <button
          class="text-[#3A2A13] border-b-2 border-[#3A2A13] pb-1 font-bold transition-all duration-300"
        >
          Cà phê
        </button>
        <button class="hover:text-[#3A2A13]">Trà sữa</button>
        <button class="hover:text-[#3A2A13]">Soda</button>
      </div>

      <!-- Menu items -->
      <div
        class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-10 max-w-6xl mx-auto"
      >
        <div
          v-for="(item, i) in menuItems"
          :key="i"
          class="flex flex-col items-start"
        >
          <!-- Khung + ảnh -->
          <div
            class="cursor-pointer group w-full bg-[#B68C62] h-[350px] flex items-center justify-center overflow-hidden rounded-md shadow-md hover:shadow-xl transition-all duration-300"
          >
            <img
              :src="item.img"
              :alt="item.name"
              class="w-25 md:w-37 mt-4 ml-4 object-contain drop-shadow-lg group-hover:scale-105 transition-transform duration-500"
            />
          </div>

          <!-- Text nằm ngoài -->
          <p
            class="cursor-pointer font-bebas text-[#594633] hover:text-[#E3B97A] text-xl font-bold uppercase mt-4 tracking-wide"
          >
            {{ item.name }}
          </p>
          <p class="cursor-pointer text-[#594633] hover:text-[#E3B97A] text-sm font-bold font-saira">
            {{ item.price }}
          </p>
        </div>
      </div>
    </div>

    <!-- Ưu đãi -->
    <div class="max-w-6xl mx-auto mt-20">
      <h3
        class="font-anton text-[#594633] text-2xl md:text-4xl uppercase tracking-wide mb-14"
      >
        Cùng với những ưu đãi
      </h3>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-10 md:gap-16">
        <div
          v-for="(deal, index) in deals"
          :key="index"
          class="flex flex-col items-center text-center"
        >
          <div
            class="w-[180px] h-[180px] md:w-[220px] md:h-[220px] rounded-full overflow-hidden flex justify-center items-center bg-gray-200 mb-6"
          >
            <img
              :src="deal.img"
              :alt="deal.title"
              class="w-full h-full object-cover"
            />
          </div>
          <h4
            class="font-anton text-[#3A2A13] text-xl md:text-2xl uppercase mb-3"
          >
            {{ deal.title }}
          </h4>
          <p
            class="text-[#3A2A13]/80 text-[14px] md:text-[15px] leading-relaxed max-w-md"
          >
            {{ deal.desc }}
          </p>
        </div>
      </div>
    </div>

    <!-- BÁNH NGỌT -->
    <div class="max-w-6xl mx-auto mt-28">
      <h3
        class="font-anton text-[#594633] text-2xl md:text-4xl uppercase tracking-wide mb-14"
      >
        Bánh ngọt, sao lại không?
      </h3>

      <div
        class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-10 md:gap-12"
      >
        <div
          v-for="(cake, idx) in sweetCakes"
          :key="idx"
          class="flex flex-col items-start"
        >
          <!-- Khung hình -->
          <div
            class="cursor-pointer group w-full bg-[#B68C62] h-[260px] md:h-[300px] flex items-center justify-center overflow-hidden rounded-md shadow-md hover:shadow-xl transition-all duration-300"
          >
            <img
              :src="cake.img"
              :alt="cake.name"
              class="w-28 md:w-36 object-contain drop-shadow-lg group-hover:scale-105 transition-transform duration-500"
            />
          </div>

          <!-- Text -->
          <p
            class="cursor-pointer font-bebas text-[#594633] hover:text-[#E3B97A] text-lg md:text-xl font-bold uppercase mt-4 tracking-wide"
          >
            {{ cake.name }}
          </p>
          <p
            class="cursor-pointer text-[#594633] hover:text-[#E3B97A] text-[14px] md:text-[15px] font-bold font-saira"
          >
            {{ cake.price }}
          </p>
        </div>
      </div>
    </div>
  </section>

  <section class="bg-[#594633] py-20 px-6 text-center text-[#F1E8C7]">
    <!-- Tiêu đề -->
    <h2 class="font-anton text-3xl md:text-5xl uppercase tracking-wide mb-20">
      Vì sao chúng tôi là nơi lí tưởng cho bạn?
    </h2>

    <!-- Grid 3 cột -->
    <div
      class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-12 md:gap-16"
    >
      <!-- Cột 1 -->
      <div class="flex flex-col items-center">
        <img
          src="/images/homepage/coffee-white.png"
          alt="Icon"
          class="w-16 mb-6 opacity-90"
        />
        <h3 class="font-anton text-xl md:text-2xl uppercase mb-8">Về Cà Phê</h3>
        <p
          class="font-playfair justify-text text-[14px] md:text-[15px] leading-relaxed text-[#F1E8C7]/90"
        >
          Cà phê tại quán của chúng tôi được pha chế từ những hạt cà phê chọn
          lọc kỹ càng và rang theo phương pháp truyền thống để đảm bảo hương vị
          đặc trưng và chất lượng tuyệt vời. Đến với quán cà phê của chúng tôi,
          bạn sẽ được thưởng thức một tách cà phê đậm đà và thơm ngon nhất.
        </p>
      </div>

      <!-- Cột 2 -->
      <div class="flex flex-col items-center">
        <img
          src="/images/homepage/bean-white.png"
          alt="Icon"
          class="w-16 mb-6 opacity-90"
        />
        <h3 class="font-anton text-xl md:text-2xl uppercase mb-8">
          VỀ MÔI TRƯỜNG
        </h3>
        <p
          class="font-playfair justify-text text-[14px] md:text-[15px] leading-relaxed text-[#F1E8C7]/90"
        >
          Quán của chúng tôi có không gian ấm cúng và thiết kế sang trọng, tạo
          ra một môi trường thư giãn và đầy cảm hứng cho khách hàng. Bạn sẽ có
          cơ hội thưởng thức cà phê tuyệt vời trong một không gian thoải mái và
          đầy hứng khởi. Hãy ghé thăm quán của chúng tôi để tận hưởng không gian
          đẹp và thoải mái nhất.
        </p>
      </div>

      <!-- Cột 3 -->
      <div class="flex flex-col items-center">
        <img
          src="/images/homepage/service-white.png"
          alt="Icon"
          class="w-16 mb-6 opacity-90"
        />
        <h3 class="font-anton text-xl md:text-2xl uppercase mb-8">
          VỀ GIAO HÀNG
        </h3>
        <p
          class="font-playfair justify-text text-[14px] md:text-[15px] leading-relaxed text-[#F1E8C7]/90"
        >
          Quán của chúng tôi có không gian ấm cúng và thiết kế sang trọng, tạo
          ra một môi trường thư giãn và đầy cảm hứng cho khách hàng. Bạn sẽ có
          cơ hội thưởng thức cà phê tuyệt vời trong một không gian thoải mái và
          đầy hứng khởi. Hãy ghé thăm quán của chúng tôi để tận hưởng không gian
          đẹp và thoải mái nhất.
        </p>
      </div>
    </div>
  </section>

  <section class="bg-[#F6EED0] py-20 px-6 font-playfair">
    <div class="max-w-4xl mx-auto text-center">
      <!-- Tiêu đề -->
      <h2
        class="text-[#594633] font-anton text-3xl md:text-4xl uppercase mb-10"
      >
        Ưu đãi dành riêng cho khách hàng qua website
      </h2>

      <!-- Mô tả -->
      <p
        class="font-playfair justify-text text-[#594633]/80 text-[16px] md:text-[15px] leading-relaxed max-w-4xl mx-auto mb-12"
      >
        Chúng tôi rất cảm kích sự quan tâm của bạn đến Tiệm cà phê Ông Quan và
        mong muốn có cơ hội chào đón bạn tới thưởng thức các loại nước uống và
        bánh ngọt tuyệt vời của chúng tôi. Hãy để lại thông tin của bạn để nhận
        ngay ưu đãi đặc biệt của chúng tôi - giảm ngay 30% trên tổng hóa đơn khi
        mua nước và bánh tại cửa hàng. Bằng cách đăng ký, bạn sẽ trở thành một
        phần của cộng đồng của Tiệm cà phê Ông Quan và được cập nhật về những sự
        kiện và ưu đãi đặc biệt sớm nhất. Chúng tôi cam kết bảo mật thông tin
        của bạn và chỉ sử dụng để gửi cho bạn các ưu đãi và tin tức mới nhất từ
        Tiệm cà phê Ông Quan. Một lần nữa, chúng tôi rất trân trọng sự quan tâm
        của bạn và hy vọng được đón tiếp bạn tại Tiệm cà phê Ông Quan sớm nhất!
      </p>
    </div>

    <!-- FORM -->
    <div
      class="max-w-4xl mx-auto border border-[#594633] p-10 md:p-16 bg-[#F6EED0]"
    >
      <h3
        class="text-center text-[#594633] font-anton text-2xl md:text-3xl uppercase mb-10"
      >
        Gửi thông tin
      </h3>

      <div class="max-w-2xl mx-auto space-y-14">
        <!-- Tên -->
        <input
          type="text"
          placeholder="Nhập tên khách hàng..."
          class="w-full bg-transparent border-b border-[#3A2A13] pb-2 text-[#3A2A13] placeholder:text-[#3A2A13]/50 focus:outline-none"
        />

        <!-- Email -->
        <input
          type="email"
          placeholder="Nhập email khách hàng..."
          class="w-full bg-transparent border-b border-[#3A2A13] pb-2 text-[#3A2A13] placeholder:text-[#3A2A13]/50 focus:outline-none"
        />

        <!-- Message -->
        <textarea
          placeholder="Nhập lời nhắn..."
          class="w-full h-40 bg-transparent border border-[#3A2A13] p-3 text-[#3A2A13] placeholder:text-[#3A2A13]/50 focus:outline-none resize-none"
        ></textarea>

        <!-- Nút gửi -->
        <div class="text-center font-anton">
          <button
            class="cursor-pointer px-10 py-2 border border-[#3A2A13] text-[#3A2A13] font-bold uppercase tracking-wide leading-relaxed hover:bg-[#eaddc2] transition"
          >
            Gửi
          </button>
        </div>
      </div>
    </div>
  </section>

  <section class="bg-[#594633] py-20 text-center">
    <h2
      class="font-baloo font-bold text-[#F1E8C7] text-3xl md:text-5xl uppercase mb-16 tracking-wide"
    >
      Về Chúng Tôi
    </h2>

    <div class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-20">
      <div
        v-for="(member, index) in team"
        :key="index"
        class="flex flex-col items-center"
      >
        <div class="relative w-40 h-40 md:w-48 md:h-48">
          <img
            :src="member.avatar"
            class="relative w-full h-full object-cover"
          />
        </div>

        <h3
          class="font-anton text-[#F1E8C7] text-xl md:text-2xl uppercase tracking-wide"
        >
          {{ member.name }}
        </h3>

        <p class="text-[#F1E8C7]/80 text-sm md:text-base mt-1 mb-4">
          {{ member.role }}
        </p>

        <div class="flex gap-6 text-[#FFFFFF] text-2xl">
          <a :href="member.instagram" target="_blank">
            <i class="fa-brands fa-instagram"></i>
          </a>
          <a :href="member.facebook" target="_blank">
            <i class="fa-brands fa-facebook"></i>
          </a>
          <a :href="member.github" target="_blank">
            <i class="fa-brands fa-github"></i>
          </a>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer component -->
  <Footer />
</template>

<script setup>
import { ref } from "vue";
import Navbar from "../../../components/client/Navbar.vue";
import Slider from "../../../components/client/Slider.vue";
import Contact from "../../../components/client/Contact.vue";
import Footer from "../../../components/client/Footer.vue";
import HomepageVideos from "../../../components/client/homepage-videos.vue";
import ProductHighlight from "../../../components/client/Product-highlight.vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Pagination } from "swiper/modules";
import "swiper/css";
import "swiper/css/pagination";

const images = [
  {
    src: "/images/homepage/outdoor-seating.png",
    alt: "Không gian ngoài trời - Ông Quan Coffee",
  },
  {
    src: "/images/homepage/windmill-bakery.png",
    alt: "Nhà gỗ trung tâm - Ông Quan Coffee",
  },
  {
    src: "/images/homepage/wooden-cabin.png",
    alt: "Góc check-in Cối Xay Gió - Ông Quan Coffee",
  },
];

const menuItems = [
  {
    name: "Cà phê đen",
    img: "/images/homepage/coffee-den.png",
    price: "25.000 VNĐ",
  },
  {
    name: "Cà phê sữa",
    img: "/images/homepage/coffee-sua.png",
    price: "25.000 VNĐ",
  },
  {
    name: "Cà phê thường",
    img: "/images/homepage/coffee-thuong.png",
    price: "25.000 VNĐ",
  },
];

const deals = [
  {
    title: "Ưu đãi #1",
    img: "/images/homepage/deal-1.png",
    desc: "Sự kết hợp giữa Cappuccino và bánh bông lan nhân khô nhỏ là một cách tuyệt vời để kết hợp hương vị ngọt ngào và tinh tế. Hãy đến Tiệm cà phê Ông Quan để thưởng thức ưu đãi này ngay hôm nay!",
  },
  {
    title: "Ưu đãi #2",
    img: "/images/homepage/deal-2.png",
    desc: "Cappuccino kết hợp với bánh sừng bò mang lại sự kết hợp hoàn hảo giữa vị béo ngậy và hương thơm dịu nhẹ. Một lựa chọn tinh tế cho buổi sáng đầy năng lượng!",
  },
];

const sweetCakes = [
  {
    name: "Bánh cuộn nho khô",
    price: "30.000 VND",
    img: "/images/homepage/menu-cake/cake-nho-kho.png",
  },
  {
    name: "Bánh nướng mè",
    price: "25.000 VND",
    img: "/images/homepage/menu-cake/cake-nuong-me.png",
  },
  {
    name: "Bánh sừng",
    price: "25.000 VND",
    img: "/images/homepage/menu-cake/cake-sung.png",
  },
  {
    name: "Bánh mật ngọt",
    price: "30.000 VND",
    img: "/images/homepage/menu-cake/cake-mat-ngot.png",
  },
  {
    name: "Bánh mứt dâu",
    price: "30.000 VND",
    img: "/images/homepage/menu-cake/cake-mut-dau.png",
  },
  {
    name: "Bánh trứng muối",
    price: "25.000 VND",
    img: "/images/homepage/menu-cake/cake-trung-muoi.png",
  },
  {
    name: "Bánh quế mật ong",
    price: "30.000 VND",
    img: "/images/homepage/menu-cake/cake-que-mat-ong.png",
  },
  {
    name: "Bánh trứng nướng",
    price: "30.000 VND",
    img: "/images/homepage/menu-cake/cake-trung-nuong.png",
  },
];

const team = [
  {
    name: "Lê Đức Trọng",
    role: "Co-founder",
    avatar: "/images/homepage/avatar.png",
    instagram: "#",
    facebook: "#",
    github: "#",
  },
  {
    name: "Lê Đức Trọng",
    role: "Co-founder",
    avatar: "/images/homepage/avatar.png",
    instagram: "#",
    facebook: "#",
    github: "#",
  },
  {
    name: "Lê Đức Trọng",
    role: "Co-founder",
    avatar: "/images/homepage/avatar.png",
    instagram: "#",
    facebook: "#",
    github: "#",
  },
];
</script>

<style>
.swiper-pagination-bullet {
  background-color: #3a2a13 !important;
  opacity: 0.6;
}
.swiper-pagination-bullet-active {
  background-color: #3a2a13 !important;
  opacity: 1;
}
.justify-text {
  text-align: justify;
  text-align-last: left;
}
</style>
