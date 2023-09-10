<template>
  <v-card class="d-flex flex-column justify-center" style="border-radius: 10px">
    <v-card-title class="d-flex flex-column align-center">
      <v-img max-width="100px" src="https://raw.githubusercontent.com/Cesar-Klemes/vb-advocacia/master/assets/img/logo-sem-fundo1.png"/>
      <h2 class="my-6">Informações</h2>
    </v-card-title>
    <v-card-text class="d-flex align-center mx-2 mt-n3">
      <v-icon>mdi-phone</v-icon>
      <span class="ml-2">
        <a class="map-link" href="tel:+5511941518775">
          (11) 9 4151-8775
        </a>
      </span>
    </v-card-text>
    <v-card-text class="d-flex align-center mx-2 mt-n3">
      <v-icon>mdi-gmail</v-icon>
      <span class="ml-2">
        <a class="map-link" href="mailto:vandeilsonbarbosa@adv.oabsp.org.br?subject=Contato via Website" target="_blank">
          vandeilsonbarbosa@adv.oabsp.org.br
        </a>
      </span>
    </v-card-text>
    <v-card-text class="d-flex align-center mx-2 mt-n3">
      <v-icon>mdi-google-maps</v-icon>
      <span class="ml-2">
        <a class="map-link" :href="googleMapsURL" target="_blank">
          Rua Olavo Bilac, 884, Jardim Magalhães - Francisco Morato/SP - CEP 07914-060
        </a>
      </span>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: "Informacoes",
  data: () => ({
    googleMapsURL: "https://www.google.com/maps/search/?api=1&query=Rua+Olavo+Bilac,+884,+Jardim+Magalhães+-+Francisco+Morato/SP+-+CEP+07914-060"
  })
}
</script>

<style scoped>

</style>
