<template>
  <div>
    <h1>Witaj w systemie zapisów zajęcia</h1>
    <p>Długość : {{ authenticatedUsername.length }}</p>
    <div v-if="!authenticatedUsername ">
      <login-form @login="logMeIn($event)" button-label="Wejdź"></login-form>
    </div>
    <div v-else >
      <loged-in-form @logout="logOut()" :email="authenticatedUsername"></loged-in-form>
      <ol>
        <li v-for="meeting in meetings" :key="meeting.id">{{ meeting }}</li>
      </ol>
    </div>

  </div>
</template>

<script>
import "milligram";
import LoginForm from "./LoginForm";
import LogedInForm from "@/LogedInForm";
export default {
  components: {LogedInForm, LoginForm},
  data() {
    return {
      authenticatedUsername: '',
      meetings : ['A', 'B','C'],
    };
  },
  methods: {
    logMeIn(username) {
      this.authenticatedUsername = username;
    },
    logOut() {
      this.authenticatedUsername = '';
    }
  }
}
</script>

<style>

</style>
