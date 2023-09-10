<template>
  <div>
    <h2 class="text-h4 white--text mb-4">Depoimentos</h2>
    <v-img src="https://storage.builderall.com//franquias/2/24123/editor-html/9384898.png" width="250px" class="mb-2"/>
    <v-carousel cycle height="400" show-arrows hide-delimiters>
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
      >
        <a :href="item.link" target="_blank" class="card-link" style="height: 100%">
          <v-card color="white" height="100%">
            <v-card-title>
              <div class="d-flex align-center">
                <v-img class="mr-3" :src="item.image" width="50px" style="border-radius: 100%"></v-img>
                <span style="color: black" class="truncate">{{ item.nome }}</span>
              </div>
            </v-card-title>
            <v-card-subtitle class="mt-1 d-flex">
              <v-icon color="#FDD835" size="20px">mdi-star</v-icon>
              <v-icon color="#FDD835" size="20px">mdi-star</v-icon>
              <v-icon color="#FDD835" size="20px">mdi-star</v-icon>
              <v-icon color="#FDD835" size="20px">mdi-star</v-icon>
              <v-icon color="#FDD835" size="20px">mdi-star</v-icon>
            </v-card-subtitle>
            <v-card-text>
              <span style="color: black">{{ item.text }}</span>
            </v-card-text>
          </v-card>
        </a>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  name: "Depoimentos",
  data: () => ({
    items: [
      {
        nome: 'Lilian Denise dos Santos',
        text: 'Maravilhoso!!!\n' +
          'Meu pai idoso muito desconfiado com outros profissionais, resolveu dar crédito ao VB Advogados.\n' +
          'Atendimento bem personalizado, com orientações claras e objetivas, preço justo para fechar com chave de ouro, resolveu processo muito antes do esperado, graças a sua eficiência e atenção .\n' +
          'Nos conquistou.\n' +
          'Super indico!!!',
        image: 'https://lh3.googleusercontent.com/a/ACg8ocLMRhv84jYl4F91f7ijmPWvurHcwmoZbHN4Nq195ZXc=w36-h36-p-rp-mo-br100',
        link: 'https://g.co/kgs/6ze52k'
      },
      {
        nome: 'Thainan Guimaraes',
        text: 'Vandeilson Barbosa, um excelente advogado, possui expertise jurídica e conhecimento aprofundado, um profissional dedicado, empenhado, zeloso, atua de forma a buscar a melhor solução para o seu caso, além disso, sua habilidade em comunicar-se de forma clara e transparente. Portanto, recomendo enfaticamente os seus serviços a qualquer pessoa que necessite de um advogado excepcional, confiável e altamente competente.',
        image: 'https://lh3.googleusercontent.com/a-/ALV-UjW_XKsWKI8KDwfNYhXqOPTO_073yBAbqzz-GSj4NKBgFVU=w36-h36-p-rp-mo-br100',
        link: 'https://g.co/kgs/cAZR9Q'
      },
      {
        nome: 'Leticia Victoretti',
        text: 'Profissionais solícitos e muito atenciosos, esclarecem dúvidas e disponibilizam o serviço de forma clara e respeitosa. Excelente atendimento!!',
        image: 'https://lh3.googleusercontent.com/a-/ALV-UjUcmkEBecHlibficEIdi5stnC5FMsEkKxV-GF0XdZcsbmaR=w36-h36-p-rp-mo-br100',
        link: 'https://g.co/kgs/Ct26FS'
      },
      {
        nome: 'Tamires Aparecida de Jesus',
        text: 'Profissional extremamente competente, responsável e com um diferencial que o destaca entre tantos: Humano!\n' +
          'Precisei do seu auxílio em um momento muito complicado para minha família, e o mesmo me orientou de forma clara, efetiva e precisa! O resultado? Fiquei respaldada dentro de tudo que poderia vir acontecer e com o comprometimento do mesmo para que tivéssemos melhores resoluções...\n' +
          'Indico Vandeilson e toda sua equipe de olhos fechados! Sem dúvidas o melhor da nossa região.',
        image: 'https://lh3.googleusercontent.com/a-/ALV-UjU_Ur_3-JHfDKlTBcxHyInJwAZsUPO1T1-b77fkaHLWZg=w36-h36-p-rp-mo-br100',
        link: 'https://g.co/kgs/6vbi5p'
      },
      {
        nome: 'Thais Oliveira',
        text: 'Entre tantos quesitos o que mais chama atenção é o comprometimento em resolver, sanando todas as dúvidas existentes, profissional extremamente competente\n' +
          'Só desejo sucesso, sucesso e mais sucesso, parabéns pelo excelente profissional que se tornou, que sua estrela brilhe cada vez mais',
        image: 'https://lh3.googleusercontent.com/a/ACg8ocKvNfxbd4e1qvCPyNGdVbm4gtiBXvGllfdK6LhoJnHK=w36-h36-p-rp-mo-br100',
        link: 'https://g.co/kgs/hig4ev'
      },
      {
        nome: 'Maria Isabel Rilco',
        text: 'Excelente cordial , detalhista nas explicações não técnicas para maior entendimento.',
        image: 'https://lh3.googleusercontent.com/a-/ALV-UjWqQ01wakM3AjvRShICdb9NqJr8vSp9V7Xlah4IF2qXf41W=w36-h36-p-rp-mo-ba3-br100',
        link: 'https://g.co/kgs/eYigyN'
      },
      {
        nome: 'Amanda Ferreira',
        text: 'Excelente atendimento, atencioso e prestativo!! Indico de olhos de fechados!',
        image: 'https://lh3.googleusercontent.com/a-/ALV-UjUDsk6u9SpJFCj2LySQRLY-9zdSrbELYoALgW3NGR89vkd8=w36-h36-p-rp-mo-br100',
        link: 'https://g.co/kgs/6MFYVC'
      },
      {
        nome: 'Lucas Trujillo Guimarães',
        text: 'Muito qualificados. Me ajudaram em um momento muito difícil. Profissional exemplar',
        image: 'https://lh3.googleusercontent.com/a/ACg8ocJuUf8jgm2vZs2Tu0_hrA0fwYf5YkGC5ZCOCjEKLSLa=w36-h36-p-rp-mo-br100',
        link: 'https://g.co/kgs/mbQdQk'
      }
    ]
  })
}
</script>

<style scoped>
.card-link {
  display: block;
  text-decoration: none;
  color: inherit;
}
.truncate {
  max-width: 80%; /* Você pode ajustar isso conforme necessário */
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
