<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
 
    <v-sheet class="mx-auto" width="300">
    <v-form @submit.prevent>
      <v-text-field
        v-model="firstName"
        :rules="rules"
        label="First name"
      ></v-text-field>
      <v-btn class="mt-2" type="submit" block>Submit</v-btn>
    </v-form>
  </v-sheet>
  

 
</template>

<style scoped>

</style>
