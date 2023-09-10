<template>
  <v-btn
    fab
    dark
    large
    color="green"
    class="fixed-btn"
    :href="'https://wa.me/5511941518775?text=' + encodeURIComponent(message)"
    target="_blank"
    :ripple="false"
  >
    <v-icon size="45px">mdi-whatsapp</v-icon>
  </v-btn>
</template>

<script>
export default {
  name: "Whatsapp",
  data: () => ({
    message: 'Olá, estou interessado em seus serviços de advocacia!'
  })
}
</script>

<style scoped>
@keyframes ripple {
  0% {
    transform: scale(0.5);
    opacity: 0.5;
  }
  50% {
    transform: scale(1);
    opacity: 1;
  }
  100% {
    transform: scale(1.5);
    opacity: 0;
  }
}

.fixed-btn::before {
  content: '';
  display: block;
  position: absolute;
  width: 200%; /* Aumentar o tamanho para que a onda seja visível em toda a extensão */
  height: 200%; /* Aumentar o tamanho para que a onda seja visível em toda a extensão */
  top: -50%; /* Centralizar no botão */
  left: -50%; /* Centralizar no botão */
  background-color: rgba(76, 175, 80, 0.7); /* cor do WhatsApp com opacidade */
  border-radius: 50%; /* torna a forma um círculo */
  animation: ripple 1.5s infinite 5s;
  z-index: -1; /* coloca a onda atrás do botão */
}

.fixed-btn {
  position: fixed;
  right: 20px;
  bottom: 20px;
  z-index: 3;
}

</style>
