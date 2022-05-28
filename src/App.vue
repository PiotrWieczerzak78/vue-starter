<template>
  <div>
    <h1>Twój email to : {{email}}</h1>
    <input type="email" v-model="email">
    <p>Długość : {{email.length}}</p>
    <div v-if="email.length < 10">Ale masz krótki adres!</div>
    <div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
    <div v-else class="zadlugi">Twój adres e-mail jest stanowczo za długi.</div>
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
.zadlugi{
  color: red;
}
</style>
