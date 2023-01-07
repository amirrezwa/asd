<template>
  <q-page class="row items-center justify-evenly">
    <q-form>
      <q-input v-model="userInfo.firstName"> First name</q-input>
      <q-input v-model="userInfo.lastName"> Last bane</q-input>
      <q-input v-model="userInfo.birthDay" type="date">Birth day</q-input>
      <q-input v-model="userInfo.email" type="email">Email</q-input>
      <q-input v-model="userInfo.userName"> Username</q-input>
      <q-input v-model="userInfo.password" type="password">Password</q-input>

      <q-btn color="primary">Send Request</q-btn>
    </q-form>

    <pre>
      {{ userInfo.firstName }}
      {{ userInfo.lastName }}
      {{ userInfo.birthDay }}
      {{ userInfo.email }}
      {{ userInfo.userName }}
      {{ userInfo.password }}
    </pre>
  </q-page>
</template>

<script setup lang="ts">
import { ref, Ref } from 'vue';
import { Person } from 'src/models/person.model';

const userInfo: Ref<Person> = ref({
  firstName: '',
  lastName: '',
  birthDay: '',
  email: '',
  userName: '',
  password: '',
});
</script>
