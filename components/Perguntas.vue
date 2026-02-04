<template>
  <div>
    <h2 class="text-h4 mb-5">Perguntas Frequentes</h2>
    <v-divider class="mb-5" />
    <v-expansion-panels>
      <v-expansion-panel
        v-for="pergunta in perguntas"
        :key="pergunta.pergunta"
        class="mb-4 color-expansion-panel"
      >
        <v-expansion-panel-header>{{
          pergunta.pergunta
        }}</v-expansion-panel-header>
        <v-expansion-panel-content>{{
          pergunta.resposta
        }}</v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </div>
</template>

<script>
export default {
  name: "Perguntas",
  data: () => ({
    perguntas: [
      {
        pergunta:
          "Posso entrar com uma ação revisional mesmo se estiver com parcelas em atraso?",
        resposta:
          "Sim, é possível. A inadimplência não impede a busca por uma ação revisional. Na verdade, muitas vezes, juros abusivos são a razão pela qual os clientes não conseguem pagar suas parcelas. A revisão pode ser uma ferramenta para lidar com essa situação.",
      },
      {
        pergunta: "Já quitei meu contrato, posso requerer a revisão?",
        resposta:
          "Sim, é possível. Até 10 anos após o pagamento da última prestação do contrato, você pode propor uma ação para reaver qualquer valor pago a mais, caso haja indícios de cobranças indevidas.",
      },
      {
        pergunta: "Não paguei nenhuma parcela ainda, posso requerer a revisão?",
        resposta:
          "Sim, você pode. Assim que o contrato estiver assinado, ele pode ser considerado apto para revisão, independentemente do pagamento das parcelas.",
      },
      {
        pergunta: "Como funciona na prática a revisão de contrato?",
        resposta:
          "Na prática, os bancos frequentemente propõem acordos para aqueles que entram com esses processos de revisão. Nesses acordos, as instituições financeiras costumam oferecer, em média, 70% de desconto sobre o valor total ainda a ser pago pelo contrato. Isso significa que se você ainda deve 30 parcelas de R$ 1.000,00 no seu financiamento, poderá quitar o contrato por R$ 9 mil apenas (um desconto de R$ 21 mil). Sim, exatamente isso.",
      },
      {
        pergunta:
          "Poderei fazer um novo empréstimo ou financiamento após a revisão do contrato?",
        resposta:
          "Após a conclusão de uma ação revisional, se o cliente estiver em dia com os novos valores acordados, não existem mais obstáculos para a obtenção de qualquer tipo de crédito. No entanto, é importante destacar que esse desimpedimento não necessariamente se aplica à mesma instituição financeira com a qual você realizou a ação revisional.",
      },
      {
        pergunta:
          "O banco poderá tomar meu veículo durante um processo revisional?",
        resposta:
          "Durante um processo revisional, o banco não pode tomar seu veículo unilateralmente. É necessário obter autorização judicial para retomar o veículo ou qualquer bem usado como garantia no contrato. Você será informado da decisão judicial antes que qualquer ação seja tomada em relação ao seu veículo.",
      },
      {
        pergunta:
          "Quanto tempo leva um processo de revisão de cobrança de juros abusivos?",
        resposta:
          "O tempo de um processo de revisão de cobrança de juros abusivos pode variar consideravelmente, dependendo da situação específica. Embora a celeridade seja um princípio do direito brasileiro, nem sempre os processos avançam rapidamente. No entanto, uma boa notícia é que a grande maioria dos casos de revisão de cobrança de juros abusivos resulta em acordos. Isso significa que muitas vezes não é necessário aguardar a conclusão do processo. Através de negociações, é possível obter um acordo que beneficie o cliente sem esperar meses. As instituições bancárias também reconhecem o risco de perderem esses processos e frequentemente estão dispostas a negociar.",
      },
      {
        pergunta: "Cai em um golpe do Pix, consigo recuperar meu dinheiro?",
        resposta:
          "Você foi uma vítima e, como tal, deve ser indenizado. É possível reaver os valores perdidos em uma transação bancária fraudulenta.",
      },
    ],
  }),
};
</script>

<style scoped>
.color-expansion-panel {
  background-color: #0c2c43 !important;
}
</style>
