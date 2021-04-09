<template>
  <div class="relative bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <div
        class="flex justify-between items-center border-b-2 border-gray-100 py-6 md:justify-start md:space-x-10"
      >
        <div class="flex justify-start lg:w-0 lg:flex-1">
          <router-link
            class="text-base font-medium text-gray-500 hover:text-gray-900"
            to="/"
          >
            <UILogoComponent />
          </router-link>
        </div>
        <UIMobileMenuButton @setIsMenu="setIsMenu()" />
        <nav class="hidden md:flex space-x-10">
          <router-link
            class="text-base font-medium text-gray-500 hover:text-gray-900"
            to="/"
            >Home</router-link
          >
          <router-link
            class="text-base font-medium text-gray-500 hover:text-gray-900"
            to="/about"
            >About</router-link
          >
          <router-link
            class="text-base font-medium text-gray-500 hover:text-gray-900"
            to="/delivery"
            >Delivery</router-link
          >
        </nav>
        <div class="hidden md:flex items-center justify-end md:flex-1 lg:w-0">
          <a
            href="#"
            class="whitespace-nowrap text-base font-medium text-gray-500 hover:text-gray-900"
          >
            Sign in
          </a>
          <UIPrimaryButtonComponent />
        </div>
      </div>
    </div>
    <HeaderMobileMenuComponent :isMenu="isMenu" @setIsMenu="setIsMenu()" />
  </div>
</template>

<script>
import UILogoComponent from "@/components/ui/UILogoComponent";
import UIMobileMenuButton from "@/components/ui/UIMobileMenuButton";
import UIPrimaryButtonComponent from "@/components/ui/UIPrimaryButtonComponent";
import HeaderMobileMenuComponent from "@/components/header/HeaderMobileMenuComponent";

export default {
  name: "HeaderComponent",
  components: {
    UILogoComponent,
    UIMobileMenuButton,
    UIPrimaryButtonComponent,
    HeaderMobileMenuComponent,
  },
  data() {
    return {
      isMenu: false,
    };
  },
  methods: {
    setIsMenu() {
      this.isMenu = !this.isMenu;
    },
  },
};
</script>
