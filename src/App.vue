<template>

  <div class="rapper">
    <SideMenuComponent></SideMenuComponent>

    <MainComponent></MainComponent>
  </div>

</template>

<script>

import 'normalize.css';
import './assets/style/common.css'
import SideMenuComponent from "@/components/SideMenuComponent.vue";
import MainComponent from "@/components/MainComponent.vue";

export default {
  name: 'App',
  components: {MainComponent, SideMenuComponent}
}
</script>
