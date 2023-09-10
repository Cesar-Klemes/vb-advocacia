<template>
  <div>
    <v-container fluid class="container-background">
      <v-container>
        <!-- Cabeçalho -->
        <header class="header-fullscreen text-center">
          <v-card class="d-flex justify-center align-center flex-column" min-height="300px" style="background-color: rgba(0, 0, 0, 0.7); width: 100%;">
            <v-img class="mt-4 responsive-image" contain src="https://raw.githubusercontent.com/Cesar-Klemes/vb-advocacia/master/assets/img/logo-sem-fundo.png"/>
            <div class="mx-2">
              <h3 class="my-5">Advogados experientes, soluções confiáveis.</h3>
            </div>
          </v-card>
        </header>
      </v-container>

      <v-container fluid style="background-color: white; color: black; border-top-left-radius: 20px; border-top-right-radius: 20px">
        <v-container>
          <!-- Sobre nós -->
          <section v-aos="'fade-up'" class="my-10">
            <h2 class="text-h4">Sobre nós</h2>
            <v-divider class="grey my-8"/>
            <v-row>
              <v-col cols="12" md="6">
                <v-img src="https://mfmiller.adv.br/wp-content/uploads/2019/04/Design-sem-nome-2.png" class="rounded"/>
              </v-col>
              <v-col>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed porta consectetur lectus, vel viverra nisl sagittis sit amet. Integer ultricies porta tortor, ac elementum magna fermentum ac. Sed eget lobortis elit. Phasellus sit amet bibendum nunc, ut mollis sem. Duis mattis enim ante, sit amet malesuada purus vulputate et. Mauris at dolor diam. Donec scelerisque faucibus odio sed eleifend. Aliquam sagittis vulputate enim, et mollis enim. Pellentesque pellentesque dapibus cursus. Duis egestas sapien sit amet tellus imperdiet, luctus tincidunt ante semper. Sed eu euismod justo.</p>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed porta consectetur lectus, vel viverra nisl sagittis sit amet. Integer ultricies porta tortor, ac elementum magna fermentum ac. Sed eget lobortis elit. Phasellus sit amet bibendum nunc, ut mollis sem. Duis mattis enim ante, sit amet malesuada purus vulputate et. Mauris at dolor diam. Donec scelerisque faucibus odio sed eleifend.</p>
              </v-col>
            </v-row>
          </section>
        </v-container>
      </v-container>

      <v-container fluid style="background-color: #212121">
        <v-container>
          <!-- Perguntas Frequentes -->
          <section v-aos="'fade-up'" class="my-10">
            <h2 class="text-h4 mb-5">Perguntas Frequentes</h2>
            <v-divider class="mb-5"/>
            <v-expansion-panels>
              <v-expansion-panel class="mb-4">
                <v-expansion-panel-header>Pergunta 1</v-expansion-panel-header>
                <v-expansion-panel-content>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ullamcorper augue sit amet elit tempus accumsan. Aenean eu tortor in dolor dapibus lacinia. Aliquam a enim sit amet mauris dapibus.</v-expansion-panel-content>
              </v-expansion-panel>
              <v-expansion-panel class="mb-4">
                <v-expansion-panel-header>Pergunta 2</v-expansion-panel-header>
                <v-expansion-panel-content>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ullamcorper augue sit amet elit tempus accumsan. Aenean eu tortor in dolor dapibus lacinia. Aliquam a enim sit amet mauris dapibus.</v-expansion-panel-content>
              </v-expansion-panel>
              <v-expansion-panel class="mb-4">
                <v-expansion-panel-header>Pergunta 3</v-expansion-panel-header>
                <v-expansion-panel-content>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ullamcorper augue sit amet elit tempus accumsan. Aenean eu tortor in dolor dapibus lacinia. Aliquam a enim sit amet mauris dapibus.</v-expansion-panel-content>
              </v-expansion-panel>
              <v-expansion-panel class="mb-4">
                <v-expansion-panel-header>Pergunta 4</v-expansion-panel-header>
                <v-expansion-panel-content>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ullamcorper augue sit amet elit tempus accumsan. Aenean eu tortor in dolor dapibus lacinia. Aliquam a enim sit amet mauris dapibus.</v-expansion-panel-content>
              </v-expansion-panel>
              <v-expansion-panel class="mb-4">
                <v-expansion-panel-header>Pergunta 5</v-expansion-panel-header>
                <v-expansion-panel-content>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ullamcorper augue sit amet elit tempus accumsan. Aenean eu tortor in dolor dapibus lacinia. Aliquam a enim sit amet mauris dapibus.</v-expansion-panel-content>
              </v-expansion-panel>
            </v-expansion-panels>
          </section>
        </v-container>
      </v-container>

      <v-container fluid style="background-color: white; color: black; border-bottom-left-radius: 20px; border-bottom-right-radius: 20px">
        <v-container>
          <!-- Contatos -->
          <section v-aos="'fade-up'" class="my-10">
            <v-row align="stretch">
              <v-col cols="12" md="4" class="d-flex">
                <v-card class="d-flex flex-column justify-center" style="border-radius: 10px">
                  <v-card-title class="d-flex flex-column align-center">
                    <v-img max-width="100px" src="https://raw.githubusercontent.com/Cesar-Klemes/vb-advocacia/master/assets/img/logo-sem-fundo1.png"/>
                    <h2 class="my-6">Informações</h2>
                  </v-card-title>
                  <v-card-text class="d-flex align-center mx-2 mt-n3">
                    <v-icon>mdi-phone</v-icon>
                    <span class="ml-2">(11) 9 9999-9999</span>
                  </v-card-text>
                  <v-card-text class="d-flex align-center mx-2 mt-n3">
                    <v-icon>mdi-gmail</v-icon>
                    <span class="ml-2">email.example@gmail.com</span>
                  </v-card-text>
                  <v-card-text class="d-flex align-center mx-2 mt-n3">
                    <v-icon>mdi-google-maps</v-icon>
                    <span class="ml-2">Rua Exemplo, 123, Parque exemplo - Cidade/SP - CEP 00000-000</span>
                  </v-card-text>
                </v-card>
              </v-col>
              <v-col>
                <h2 class="text-h4 mb-5">Contatos</h2>
                <v-form>
                  <!-- Campo Nome -->
                  <v-text-field
                    solo-inverted
                    class="custom-field"
                    label="Nome"
                    v-model="nome"
                    required
                  ></v-text-field>

                  <!-- Campo E-mail -->
                  <v-text-field
                    solo-inverted
                    class="custom-field"
                    label="E-mail"
                    v-model="email"
                    required
                    :rules="[rules.required, rules.email]"
                  ></v-text-field>

                  <!-- Campo Telefone -->
                  <v-text-field
                    solo-inverted
                    class="custom-field"
                    label="Telefone"
                    v-model="telefone"
                    required
                    :rules="[rules.onlyNumbers]"
                    mask="(##) #####-####"
                    placeholder="(XX) XXXXX-XXXX"
                  ></v-text-field>

                  <!-- Campo Assunto -->
                  <v-text-field
                    solo-inverted
                    class="custom-field"
                    label="Assunto"
                    v-model="assunto"
                    required
                  ></v-text-field>

                  <!-- Campo Mensagem -->
                  <v-textarea
                    solo-inverted
                    class="custom-field"
                    label="Mensagem"
                    v-model="mensagem"
                    required
                  ></v-textarea>

                  <!-- Botão de Envio -->
                  <v-btn @click="enviarFormulario">Enviar</v-btn>
                </v-form>
              </v-col>
            </v-row>
          </section>
        </v-container>
      </v-container>
    </v-container>
    <!-- Rodapé -->
    <v-footer class="ma-0 pa-0" style="width: 100%; background-color: #212121;">
      <v-container class="mt-4">
        <v-row>
          <v-col cols="12" md="6">
            <h3>SOBRE</h3>
            <p class="mt-3">Scanfcode.com CODE WANTS TO BE SIMPLE is an initiative to help the upcoming programmers with the code. Scanfcode focuses on providing the most efficient code or snippets as the code wants to be simple. We will help programmers build up concepts in different programming languages that include C, C++, Java, HTML, CSS, Bootstrap, JavaScript, PHP, Android, SQL and Algorithm.</p>
          </v-col>
          <v-col>
            <h3>OUTROS CONTATOS</h3>
            <a :href="'https://www.facebook.com/VandeilsonBarbosa'" target="_blank" class="d-flex align-center mt-3 text-decoration-none white--text">
              <v-icon>mdi-facebook</v-icon>
              <span class="ml-1">Vandeilson Barbosa</span>
            </a>
            <a :href="'https://www.linkedin.com/in/vandeilson-barbosa/'" target="_blank" class="d-flex align-center mt-3 text-decoration-none white--text">
              <v-icon>mdi-linkedin</v-icon>
              <span class="ml-1">vandeilson-barbosa/</span>
            </a>
          </v-col>
        </v-row>
        <v-row>
          <v-col>
            <p>&copy; 2023 VB Advogados. Todos os direitos reservados.</p>
          </v-col>
          <v-col class="text-end">
            Desenvolvido por <a :href="'https://www.linkedin.com/in/cesar-klemes/'" target="_blank" class="align-center mt-3 text-decoration-none white--text"><span style="font-weight: bold">Cesar Klemes</span></a>
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
  </div>

</template>

<script>
import AOS from 'aos'
import 'aos/dist/aos.css'

export default {
  mounted() {
    this.$nextTick(() => {
      AOS.init({
        duration: 1200
      })
    });
  },
  directives: {
    aos(el, binding) {
      el.setAttribute('data-aos', binding.value)
    }
  },
  data: () => ({
    nome: '',
    email: '',
    telefone: '',
    assunto: '',
    mensagem: '',
    rules: {
      required: value => !!value || 'Campo obrigatório.',
      onlyNumbers: value => (/^[0-9]*$/.test(value)) || 'Insira apenas números',
      email: value => {
        const pattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/
        return pattern.test(value) || 'E-mail inválido.'
      }
    }
  }),
  methods: {
    enviarFormulario() {
      if (this.$refs.form.validate()) {
        // Código para enviar o formulário (por exemplo, fazer uma chamada API)
      }
    }
  }
}
</script>
<style>
.container-background {
  background-image: url('https://rodrigocosta.com/wp-content/uploads/2021/09/areas-de-atuacao.png');
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
  min-height: 100vh;
}

.header-fullscreen {
  height: calc(100vh - 64px);
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Cor da borda inferior (linha) dos campos */
.custom-field .v-input__slot::before {
  border-color: black !important;
}

/* Cor da borda inferior dos campos quando focados */
.custom-field .v-input__slot:focus-within::before {
  border-color: black !important;
}
/* Cor do texto dos campos e do rótulo */
.custom-field input,
.custom-field textarea,
.custom-field label,
.custom-field .v-label {
  color: black !important;
}

/* Cor do ícone dos campos */
.custom-field .v-icon {
  color: black !important;
}

/* Cor da borda inferior dos campos quando focados */
.custom-field .v-input__slot:focus-within::before {
  border-color: black !important;
}
/* Cor da borda inferior (linha) e do texto dos campos inválidos */
.error--text::before {
  border-color: red !important;
}

.error--text .v-label,
.error--text .v-icon,
.error--text input,
.error--text textarea {
  color: red !important;
}

/* Cor do texto de erro */
.error--text .v-messages__message {
  color: red !important;
}

/* Estilo para a barra de rolagem em si */
::-webkit-scrollbar {
  width: 10px;
  background-color: #F5F5F5;
}

/* Estilo para a "pegada" ou "handle" da barra de rolagem */
::-webkit-scrollbar-thumb {
  background-color: #555;
  border-radius: 10px;
  transition: background-color 0.3s;
}

/* Efeito hover para a pegada da barra de rolagem */
::-webkit-scrollbar-thumb:hover {
  background-color: #444;
}

/* Estilo para a "trilha" ou "track" da barra de rolagem */
::-webkit-scrollbar-track {
  border-radius: 10px;
  background-color: #F5F5F5;
}

/* Estilo padrão para desktop */
.responsive-image {
  width: 500px;
}

/* Estilo para telas menores (por exemplo, abaixo de 600px) */
@media (max-width: 600px) {
  .responsive-image {
    width: 300px; /* ou o tamanho que você desejar para dispositivos móveis */
  }
}
</style>

