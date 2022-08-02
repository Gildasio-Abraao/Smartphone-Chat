<template>
  <div class="container light-mode">
    <div class="smartphone-case">
      <div class="smartphone-screen light-mode">
        <SmartphoneButtons/>
        <UserMessages :messages="messages" :height="boxHeight"/>
        <InputMessage @setMessage="setUserMessage"/>
      </div>
    </div>
  </div>
</template>

<script>
import 'primeicons/primeicons.css';
import UserMessages from './components/UserMessages.vue';
import InputMessage from './components/InputMessage.vue';
import SmartphoneButtons from './components/SmartphoneButtons.vue';

export default {
  name: 'App',
  components: {
    InputMessage,
    SmartphoneButtons,
    UserMessages
  },
  data: () => ({
    messages: [],
    boxHeight: 0
  }),
  methods: {
    setUserMessage(userMessage) {
      const messageBox = document.querySelector('.messages-box');
      this.messages.push(userMessage);

      //Scroll to last message
      this.boxHeight = messageBox.scrollHeight;
      messageBox.scroll(0, this.boxHeight);
    }
  }
}
</script>

<style>
@import 'assets/style.css';
</style>
