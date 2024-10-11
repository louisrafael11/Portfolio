<template>
    <v-container id="contact" class="my-5">
      <h1 class="white--text">Contact</h1>
      <v-form>
        <v-text-field label="Name" class="white--text"></v-text-field>
        <v-text-field label="Email" class="white--text"></v-text-field>
        <v-textarea label="Message" class="white--text"></v-textarea>
        <v-btn @click="submit">Send</v-btn>
      </v-form>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'ContactPage',
    methods: {
      submit() {
        // Handle form submission
      },
    },
  };
  </script>
  
  <style>
  .white--text {
    color: white;
  }
  </style>
  