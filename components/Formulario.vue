<template>
  <div>
    <h2 class="text-h4 mb-5">Contatos</h2>
    <v-form ref="form">
      <!-- Campo Nome -->
      <v-text-field
        solo-inverted
        class="custom-field"
        label="Nome"
        v-model="nome"
        required
        :rules="[rules.required, rules.min3]"
        validate-on-blur
      ></v-text-field>

      <!-- Campo E-mail -->
      <v-text-field
        solo-inverted
        class="custom-field"
        label="E-mail"
        v-model="email"
        required
        :rules="[rules.email]"
        validate-on-blur
      ></v-text-field>

      <!-- Campo Telefone -->
      <v-text-field
        solo-inverted
        class="custom-field"
        label="Telefone"
        v-model="telefone"
        required
        v-mask="'(##) #####-####'"
        placeholder="(XX) XXXXX-XXXX"
        :rules="[rules.minTelefone]"
        validate-on-blur
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
      <v-btn @click="enviarFormulario" color="#0c2c43">Enviar</v-btn>
    </v-form>
  </div>
</template>

<script>
export default {
  name: "Formulario",
  data: () => ({
    nome: '',
    email: '',
    telefone: '',
    assunto: '',
    mensagem: '',
    rules: {
      required: value => !!value || 'Campo obrigatório.',
      min3: value => (value && value.length >= 3) || 'Nome deve ter pelo menos 3 caracteres',
      minTelefone: value => {
        if (!value) return true
        return (value.length >= 15) || 'Telefone inválido';
      },
      email: value => {
        if (!value) return true
        const pattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/
        return pattern.test(value) || 'E-mail inválido.'
      }
    }
  }),
  methods: {
    enviarFormulario() {
      if (this.$refs.form.validate()) {
        const numeroTelefone = '+5511941518775'
        let mensagem = encodeURIComponent('Olá, meu nome é ' + this.nome + '. ')
        if (this.assunto) {
          mensagem = mensagem + 'O assunto que eu gostaria de falar é sobre ' + this.assunto + '. '
        } else {
          mensagem = mensagem + 'Gostaria de mais informações! '
        }
        if (this.email) {
          mensagem = mensagem + 'Caso prefira, pode entrar em contato comigo pelo e-mail ' + this.email + '. '
        }
        if (this.telefone) {
          mensagem = mensagem + 'Meu telefone é ' + this.telefone + '. '
        }
        if (this.mensagem) {
          mensagem = mensagem + 'Mensagem: ' + this.mensagem + '. '
        }

        const urlWhatsapp = `https://api.whatsapp.com/send?phone=${numeroTelefone}&text=${mensagem}`

        window.open(urlWhatsapp, '_blank')
      }
    }
  }
}
</script>

<style scoped>

</style>
