<template>
  <div>
    <h1>Witaj w systemie do zapisów na zajęcia</h1>
   

  <div v-if="!isAuthenticated">
    Zaloguj się e-mailem
    <input type="email" v-model="email">
    <button @click="login()">Wchodzę</button>
    </div>

<div v-else>
 <h2>Witaj {{ email }}</h2>
 <a @click="logout()">Wyloguj się</a>
</div>

  </div>

</template>

<script>
import "milligram";

export default {
  data() {
    return {
      email: "",
      
      isAuthenticated: false
    };
  },
  methods: {
  login() {
    this.isAuthenticated = true;
  },
  logout() {
    this.isAuthenticated = false;
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