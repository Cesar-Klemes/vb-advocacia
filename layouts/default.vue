<template>
  <v-app>
    <v-app-bar app color="accent" dark>
      <v-toolbar-title>VB Advogados</v-toolbar-title>
      <v-spacer></v-spacer>
      <!-- Botão de menu (ícone de hambúrguer) para visualização mobile -->
      <v-btn icon @click.stop="drawer = !drawer" class="d-flex d-sm-none">
        <v-icon>mdi-menu</v-icon>
      </v-btn>

      <!-- Itens de menu para visualização desktop -->
      <v-btn text to="/" class="d-none d-sm-flex">Início</v-btn>
      <v-btn text to="/contatos" class="d-none d-sm-flex">Contatos</v-btn>
      <v-btn text to="/menu" class="d-none d-sm-flex">Menu</v-btn>
      <v-btn text to="/redes" class="d-none d-sm-flex">Redes</v-btn>
    </v-app-bar>

    <!-- Menu lateral para visualização mobile -->
    <v-navigation-drawer v-model="drawer" app temporary right>
      <v-list>
        <v-list-item @click="drawer = false" to="/">
          <v-list-item-content>Início</v-list-item-content>
        </v-list-item>
        <v-list-item @click="drawer = false" to="/contatos">
          <v-list-item-content>Contatos</v-list-item-content>
        </v-list-item>
        <v-list-item @click="drawer = false" to="/menu">
          <v-list-item-content>Menu</v-list-item-content>
        </v-list-item>
        <v-list-item @click="drawer = false" to="/redes">
          <v-list-item-content>Redes</v-list-item-content>
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
  }
}
</script>
