<template>
  <h2>Witaj {{email}}</h2>
  <a @click="logOut()" >Wyloguj</a>
</template>

<script>

export default {
  props: ['email'],
  name: "LogedInForm",
  methods: {
    logOut() {
      this.$emit('logout');
    }
  }
}

</script>

<style scoped>

</style>