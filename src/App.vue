<template>
  <div>
    <h1>Witaj w systemie do zapisów na zajęcia</h1>
   

  <div v-if="logged === false">
    <p>Zaloguj się e-mailem</p>
    <input type="email" v-model="email">
    <button @click="login()">Wchodzę</button>
    </div>

<div v-if="logged === true">
 <h2>Witaj {{ email }}</h2>
 <button @click="logout()">Wyloguj się</button>
</div>

  </div>

</template>

<script>
export default {
  data() {
    return {
      email: "",
      logged: false
    };
  },
  methods: {
  login() {
    this.logged = true;
  },
  logout() {
    this.logged = false;
  }
}
}
</script>

<style>
.red{
  color:red;
}
</style>
// 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