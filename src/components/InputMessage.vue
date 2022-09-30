<template>
  <form class="bottom-space" method="dialog">
    <InputText type="text" v-model="message" class="user-message"/>
    <button class="pi pi-comment" @click="setMessage"/>
  </form>
</template>

<script>
import InputText from 'primevue/inputtext';

export default {
  name: 'inputMessage',
  components: {
    InputText
  },
  data: () => ({
    message: ''
  }),
  methods: {
    setMessage() {
      if(this.message.length > 0) {
          this.$emit('setMessage', {
            userMessage: this.message
        });
      }
      this.message = '';
    }
  }
}
</script>

<style scoped>
.bottom-space {
    width: 90%;
    position: absolute;
    bottom: 10px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.d-flex.align-center {
    display: flex;
    align-items: center;
}
.user-message {
    width: 85%;
    height: 22px;
    color: #fff;
    border-radius: 25px;
    border: none;
    background-color: #2d2e32;
    font-weight: 400;
    outline: none;
    padding: 4px 10px 4px 20px;
}
.pi-comment {
    color: #248bf5;
    background: transparent;
    border: none;
    margin-left: 5px;
    font-size: 1.5rem;
    cursor: pointer;
    outline: none;
    transition: 0.3s;
}
.pi-comment:hover {
    color: #5b9b66;
}
</style>