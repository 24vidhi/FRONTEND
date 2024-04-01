<script setup lang="ts">
import { ref } from "vue";

const form = ref({
    email: '',
    password: '',
    remember: false
});

function submit () {
    alert(JSON.stringify(form.value));
}

</script>

<template>
    <div class="pa-2 pb-8 background-image">
        <v-card class="pa-12 pb-8"
        height="560"
        width="40%"
        elevation="16"
        style="margin-left: 50px;"
        >
        <v-card-title class="text-center"
        style="font-size: 44px; color:darkblue; font-family:Georgia, 'Times New Roman', Times, serif;" 
        >
    <span class="headline">Login here</span>
    </v-card-title>

    <v-sheet class="pa-4 text-center mx-auto"
    max-width="500"
    rounded="lg"
    width="100%">
      <v-form @submit.prevent="submit">

        <!-- TEXT FIELDS -->
        <div class="text-subtitle-1 text-medium-emphasis text-left">Email</div>
        <v-text-field
          clearable
          prepend-inner-icon="mdi-email-outline"
          v-model="form.email"
          label="Enter your email address"
        ></v-text-field>

        <div class="text-subtitle-1 text-medium-emphasis d-flex align-center justify-space-between">Password</div>
        <v-text-field
          clearable      
          prepend-inner-icon="mdi-lock-outline"
          v-model="form.password"
          type="password"
          label="Enter your password"
        ></v-text-field>

        <v-checkbox
            v-model="form.remember"
            color="red"
            label="Remember me"
            hide-details
          ></v-checkbox>
<br>
        <v-btn class="mt-2" 
        type="submit" 
        color="blue"
        size="x-large"
        variant="tonal"
        elevation="5"
        block>LOG IN</v-btn>
      </v-form>

      <v-card-text class="text-center">
        <p class="text-body-2" >Don't have an account?
            <a class="text-blue text-decoration-none" href="/register">Register</a>
        </p>
      </v-card-text>

    </v-sheet>
</v-card>
</div>

  </template>

<style>
.background-image {
  background-image: url('../assets/15.jpg');
  background-size: cover;
  background-position: center;
  height: 93vh;
  display: flex;
  justify-content: flex-start;
  align-items: center;
}
.v-sheet {
  width: 100%; /* Make the sheet take the full width */
  max-width: 450px;
}

</style>