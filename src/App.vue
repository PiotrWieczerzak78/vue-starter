<template>
  <div>
    <h1>Twój email to : {{email}}</h1>
    <input type="email" v-model="email">
    {{email.length}}
  </div>
</template>

<script>

export default {
  data() {
    return {
      email: '',
      password: ''
    };
  }

}
</script>

<style>

</style>
