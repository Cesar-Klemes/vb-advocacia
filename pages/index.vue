<template>
  <div>
    <v-container fluid class="container-background">
      <v-container>
        <!-- Cabeçalho -->
        <section id="inicio">
          <header class="header-fullscreen text-center">
            <v-card class="d-flex justify-center align-center flex-column" min-height="300px" style="background-color: rgba(0, 0, 0, 0.7); width: 100%;">
              <v-img class="mt-4 responsive-image" contain src="https://raw.githubusercontent.com/Cesar-Klemes/vb-advocacia/master/assets/img/logo-sem-fundo.png"/>
              <div class="mx-2">
                <h3 class="my-5">Advogados experientes, soluções confiáveis.</h3>
              </div>
            </v-card>
          </header>
        </section>
      </v-container>

      <v-container fluid style="background-color: white; color: black; border-top-left-radius: 20px; border-top-right-radius: 20px">
        <v-container>
          <!-- Sobre nós -->
          <section v-aos="'fade-up'" class="my-10" id="sobre">
            <Sobre/>
          </section>
        </v-container>
      </v-container>

      <v-container fluid style="background-color: #212121">
        <v-container>
          <!-- Perguntas Frequentes -->
          <section v-aos="'fade-up'" class="my-10" id="perguntas">
            <Perguntas/>
          </section>
        </v-container>
      </v-container>

      <v-container fluid style="background-color: white; color: black; border-bottom-left-radius: 20px; border-bottom-right-radius: 20px">
        <v-container>
          <!-- Contatos -->
          <section v-aos="'fade-up'" class="my-10" id="contatos">
            <v-row align="stretch">
              <v-col cols="12" md="4" class="d-flex">
                <Informacoes/>
              </v-col>
              <v-col>
                <Formulario/>
              </v-col>
            </v-row>
          </section>
        </v-container>
      </v-container>
    </v-container>

    <Whatsapp/>

    <!-- Rodapé -->
    <v-footer class="ma-0 pa-0" style="width: 100%; background-color: #212121;">
      <v-container class="mt-4">
        <Footer/>
      </v-container>
    </v-footer>
  </div>

</template>

<script>
import Sobre from '~/components/Sobre.vue'
import Perguntas from '~/components/Perguntas.vue'
import Informacoes from '~/components/Informacoes.vue'
import Formulario from "~/components/Formulario.vue"
import Footer from "~/components/Footer.vue"
import Whatsapp from "~/components/Whatsapp.vue"

import AOS from 'aos'
import 'aos/dist/aos.css'
import VueMask from 'v-mask'
import Vue from "vue"
Vue.use(VueMask)

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
  components: {
    Sobre,
    Perguntas,
    Informacoes,
    Formulario,
    Footer,
    Whatsapp
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

.map-link,
.map-link:visited {
  color: inherit !important;
  text-decoration: none;
}

.map-link:hover {
  color: #007BFF !important;
  text-decoration: underline;
}
</style>

