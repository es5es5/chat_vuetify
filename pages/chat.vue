<template>
  <div class="chat">
    <h2>채팅방</h2>
    <input v-model="sendMessage" type="text">
    <v-btn color="success" @click="enter">
      ddd
    </v-btn>
  </div>
</template>

<script>
import socket from '~/plugins/socket.io.js'

export default {
  name: 'Chat',
  data() {
    return {
      username: '',
      sendMessage: ''
    }
  },
  methods: {
    enter() {
      socket.emit('everyBody', this.username)
    }
  }
}
</script>

<style>

</style>
