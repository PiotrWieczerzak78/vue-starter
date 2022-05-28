<template>
  <div>
    <h3>Zaloguj się e-mailem
      <input type="email" v-model="email" @keydown.enter="alertMyEmail">
      <button @click="enter()" >{{ buttonLabel }}</button>
    </h3>
  </div>
</template>

<script>

export default {
  props: ['buttonLabel'],
  data() {
    return {
      email: '',
    }
  },
  methods: {
    enter() {
      this.$emit('login', this.email);
    }
  }
}
</script>