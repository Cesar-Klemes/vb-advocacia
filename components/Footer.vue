<template>
  <div>
    <v-row class="justify-center">
      <v-col cols="auto" md="auto" class="d-flex justify-center">
        <v-img width="150px" height="150px" src="https://raw.githubusercontent.com/Cesar-Klemes/vb-advocacia/master/assets/img/vandeilson.jpg" style="border-radius: 100%"/>
      </v-col>
      <v-col cols="12" md="8">
        <h3>Sobre Dr. Vandeilson Barbosa</h3>
        <p class="mt-3">O Dr. Vandeilson Barbosa é um advogado altamente qualificado, devidamente registrado na OAB/SP com o número 463.639. Além de sua formação em Direito, ele possui uma pós-graduação em Advocacia Cível pela ESA - Escola Superior da Advocacia. Com especialização em Direito do Consumidor Bancário, ele está dedicado a oferecer aos seus clientes uma representação jurídica confiável e de alta qualidade.</p>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" md="6">
        <p>&copy; 2023 VB Advogados. Todos os direitos reservados.</p>
      </v-col>
      <v-col class="text-center text-md-end mr-1">
        Desenvolvido por <a :href="'https://www.linkedin.com/in/cesar-klemes/'" target="_blank" class="align-center mt-3 text-decoration-none white--text"><span style="font-weight: bold">Cesar Klemes</span></a>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style scoped>

</style>
