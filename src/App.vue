<template>
  <div id="app flex flex-col h-screen justify-between">
    <HeaderComponent />
    <div class="flex-grow">
      <router-view />
    </div>
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "@/components/header/HeaderComponent";
import FooterComponent from "@/components/FooterComponent";

export default {
  components: {
    HeaderComponent,
    FooterComponent,
  },
};
</script>
