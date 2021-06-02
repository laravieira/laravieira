<template>
  <h1 class="message"><strong>{{ message[0] }}</strong>{{ message[1] }}</h1>
</template>

<script>
let messageBadRequest    = [400, "Tenta de novo, mas verifica antes."];
let messageUnauthorized  = [401, "Espertinho... nem te conheço!"];
let messageForbidden     = [403, "Não, não... Não pode!"];
let messageNotFound      = [404, "Uée... esse link não existe."];
let messageInternalError = [500, "Epa! Parece que vc achou um bug."];

let buildMessages = [
  "Imaginando",    "Arquitetando", "Inventando", "Idealizando",
  "Tramando",      "Formulando",   "Compondo",   "Tornando-o",
  "Implementando", "Efetivando",   "Calculando", "Engenhando",
  "Arrumando",     "Despertando",  "Simulando",  "Contando",
];
function chooseMessage() {
  switch(window.location.pathname) {
    case '/':
      return ['', getRandomMessage(buildMessages)];
    case '/400':
      return messageBadRequest;
    case '/401':
      return messageUnauthorized;
    case '/403':
      return messageForbidden;
    case '/500':
      return messageInternalError;
    default:
      return messageNotFound;
  }
}
function getRandomMessage(messages) {
  return messages[Math.floor(Math.random()*(messages.length-1))];
}
export default {
  name: 'App',
  data() {
    return {
      message: chooseMessage(),
    }
  },
}
</script>

<style scoped>
.message {
  color: #E9ECF2;
  font-size: 1.8rem;
  margin-top: 2rem;
  font-weight: lighter;
  font-family: 'Montserrat', sans-serif;
  text-transform: uppercase;
  letter-spacing: 0.3rem;
}
.message strong {
  font-size: 2rem;
  display: block;
}
</style>
