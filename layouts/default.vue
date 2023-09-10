<template>
  <v-app>
    <v-app-bar app color="#0c2c43" dark>
      <v-img max-width="50px" src="https://raw.githubusercontent.com/Cesar-Klemes/vb-advocacia/master/assets/img/logo-sem-fundo1.png"/>
      <v-toolbar-title class="ml-3">Advogados</v-toolbar-title>
      <v-spacer></v-spacer>
      <!-- Botão de menu (ícone de hambúrguer) para visualização mobile -->
      <v-btn icon @click.stop="drawer = !drawer" class="d-flex d-sm-none">
        <v-icon>mdi-menu</v-icon>
      </v-btn>

      <!-- Itens de menu para visualização desktop -->
      <v-btn text @click="scrollToSection('inicio')" class="d-none d-sm-flex">Início</v-btn>
      <v-btn text @click="scrollToSection('sobre')" class="d-none d-sm-flex">Sobre nós</v-btn>
      <v-btn text @click="scrollToSection('servicos')" class="d-none d-sm-flex">Serviços</v-btn>
      <v-btn text @click="scrollToSection('perguntas')" class="d-none d-sm-flex">Perguntas</v-btn>
      <v-btn text @click="scrollToSection('contatos')" class="d-none d-sm-flex">Contatos</v-btn>
    </v-app-bar>

    <!-- Menu lateral para visualização mobile -->
    <v-navigation-drawer v-model="drawer" app temporary right color="#0c2c43">
      <v-list>
        <v-list-item @click="drawer = false; scrollToSection('inicio')">
          <v-list-item-content>Início</v-list-item-content>
        </v-list-item>
        <v-list-item @click="drawer = false; scrollToSection('sobre')">
          <v-list-item-content>Sobre nós</v-list-item-content>
        </v-list-item>
        <v-list-item @click="drawer = false; scrollToSection('servicos')">
          <v-list-item-content>Serviços</v-list-item-content>
        </v-list-item>
        <v-list-item @click="drawer = false; scrollToSection('perguntas')">
          <v-list-item-content>Perguntas</v-list-item-content>
        </v-list-item>
        <v-list-item @click="drawer = false; scrollToSection('contatos')">
          <v-list-item-content>Contatos</v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <nuxt />
    </v-main>
  </v-app>
</template>



<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      drawer: false
    }
  },
  methods: {
    scrollToSection(sectionId) {
      const element = document.getElementById(sectionId);
      let yOffset = -120
      if (sectionId === 'inicio') {
        yOffset = 0;
      }
      const y = element.getBoundingClientRect().top + window.pageYOffset + yOffset;

      window.scrollTo({ top: y, behavior: 'smooth' });
    }
  }
}
</script>
<style>
html {
  scroll-behavior: smooth;
}
</style>
