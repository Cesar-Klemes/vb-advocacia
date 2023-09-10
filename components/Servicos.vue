<template>
  <div>
    <h2 class="text-h4">Serviços</h2>
    <v-divider class="grey my-10"/>
    <v-row>
      <v-col v-for="servico in servicos" cols="12" md="6" class="d-flex justify-center">
        <v-card max-width="400px" color="white" class="d-flex flex-column justify-space-between">
          <v-card-title class="justify-center">
            <span style="color: black">{{ servico.title }}</span>
          </v-card-title>
          <div class="text-center">
            <v-icon size="70px" color="black">{{ servico.icon }}</v-icon>
          </div>
          <v-card-text class="justify-center d-flex flex-column align-center" style="height: 170px">
            <p style="color: black">{{ servico.description }}</p>
          </v-card-text>
          <v-card-actions class="justify-center mb-2">
            <v-btn
              outlined
              color="black"
              :href="'https://wa.me/5511941518775?text=' + encodeURIComponent(servico.message)"
              target="_blank"
            >
              Saber Mais
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Servicos",
  data: () => ({
    servicos: [
      {
        title: 'Revisional de Veículos',
        icon: 'mdi-car',
        description: 'A revisão do contrato de financiamento oferece a possibilidade de reduzir o montante final em até 70%, permitindo que você se livre de juros excessivos. É possível iniciar o processo de revisão, mesmo que o contrato esteja em atraso.',
        message: 'Olá! Gostaria de saber mais sobre seus serviços de Revisional de Veículos.'
      },
      {
        title: 'Empréstimos Bancários',
        icon: 'mdi-bank',
        description: 'Se você está pagando um valor de empréstimo bancário excessivamente elevado, é possível que esteja pagando juros abusivos. Você pode buscar uma ação revisional para reduzir esse montante.',
        message: 'Olá! Gostaria de saber mais sobre seus serviços de Empréstimos Bancários.'
      },
      {
        title: 'Defesa em Busca e Apreensão',
        icon: 'mdi-train-car-flatbed-car',
        description: 'A Busca e Apreensão de Veículos ocorre devido à inadimplência em contratos de financiamento, leasing ou alienação fiduciária, mas é fundamental compreender que, mesmo nessas circunstâncias, você tem direitos legais e a oportunidade de buscar soluções para recuperar ou manter seu veículo.',
        message: 'Olá! Gostaria de saber mais sobre seus serviços de Defesa em Busca e Apreensão.'
      },
      {
        title: 'Fraudes Bancárias/Golpe do pix',
        icon: 'mdi-cash-fast',
        description: 'Se você foi vítima de uma fraude bancária ou caiu no golpe do Pix, é importante saber que existem possibilidades de buscar a reparação pelos danos sofridos.',
        message: 'Olá! Gostaria de saber mais sobre seus serviços de Fraudes Bancárias/Golpe do pix.'
      },
    ]
  })
}
</script>

<style scoped>

</style>
