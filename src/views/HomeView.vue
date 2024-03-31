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
    <div class="pa-15 pb-8">
        <v-card class="pa-12 pb-8 mx-auto"
        height="560"
        width="50%"
        elevation="16"
        >
        <v-card-title class="text-center"
        style="font-size: 44px; color:blue; font-family:Georgia, 'Times New Roman', Times, serif;" 
        >
    <span class="headline">Login here</span>
    </v-card-title>

    <v-sheet class="pa-4 text-center mx-auto"
    max-width="600"
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