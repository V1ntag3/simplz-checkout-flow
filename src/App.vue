<template>
  <v-app>

    <MenuBar />

    <v-main id="simpliz-bg" class="background">
      <v-container id="container-layout" fluid class="container">
        <transition name="fade-slide" mode="out-in">
          <router-view />
        </transition>
      </v-container>
    </v-main>

    <!-- <v-footer app color="primary" dark>
      <v-col class="text-center white--text">
        © {{ new Date().getFullYear() }} Simpliz. Todos os direitos reservados.
      </v-col>
    </v-footer> -->
  </v-app>
</template>

<script>
import '@/styles/simpliz-theme.scss';
import '@/styles/vuetify-mods.scss';
import '@/styles/index-style.scss';
import MenuBar from './components/ui/MenuBar.vue';

export default {
  name: "App",
  components: {
    MenuBar
  }
};
</script>
<style scoped>
/* Transicoes de tela */

.fade-slide-enter-active,
.fade-slide-leave-active {
  transition: all 0.4s ease;
  position: relative;
}

.fade-slide-enter-from {
  opacity: 0;
  transform: translateX(30px);
}

.fade-slide-enter-to {
  opacity: 1;
  transform: translateX(0);
}

.fade-slide-leave-from {
  opacity: 1;
  transform: translateX(0);
}

.fade-slide-leave-to {
  opacity: 0;
  transform: translateX(-30px);
}
</style>
