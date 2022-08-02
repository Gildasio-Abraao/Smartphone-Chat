<template>
    <div class="messages-box">
      <div class="message" v-for="(message, index) in messages" :key="index">
        <p class="from-me">{{ message.userMessage }}</p>
      </div>
    </div>
</template>

<script>
export default {
  name: 'UserMessages',
  props: {
    messages: {
      type: Array,
      default: () => [],
      description: 'Mensagem recebida do user',
    }
  },
}
</script>

<style>
/*Screen*/
.messages-box {
  width: 97%;
  height: 89%;
  overflow-y: auto;
  padding: 0;
  margin: 15px 0;
}

.messages-box::-webkit-scrollbar {
  width: 3px;
}

.messages-box::-webkit-scrollbar-track {
  background-color: #d9d9d9;
}

.messages-box::-webkit-scrollbar-thumb {
  box-shadow: inset 0 0 1px #000000;
}

.message p {
  font-size: 0.9rem;
  border-radius: 1.15rem 1.15rem 0rem 1.15rem;
  line-height: 1.25;
  max-width: 84%;
  padding: 0.5rem 0.875rem;
  position: relative;
  word-wrap: break-word;
}

.message p::before {
  content: "";
  height: 1rem;
  position: absolute;
  top: 2px;
  right: 0px;
}

p.from-me {
  align-self: flex-end;
  background-color: #248bf5;
  color: #fff; 
}

p[class^="from-"] {
  margin: 0.5rem 0.5rem 0.5rem auto;
  width: -webkit-fit-content;
  width: -moz-fit-content;
  width: fit-content;
}

p.from-me ~ p.from-me {
  margin: 0.25rem 0 0;
}

</style>