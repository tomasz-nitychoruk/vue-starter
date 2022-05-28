<template>
  <div>
    <h1>Witaj w systemie do zapisów na zajęcia</h1>
   
 
  <div v-if="!isAuthenticated">
   <login-form @login="logIn($event)"></login-form>
    </div>

<div v-else>
 <logged-panel @logout="logOut()"
 :username="isAuthenticated"></logged-panel>
</div> 


  </div>

</template>

<script>
import "milligram";
import LoginForm from "./LoginForm";
import LoggedPanel from "./LoggedPanel";

export default {
  components: {LoginForm,
  LoggedPanel},

  data() {
    return {  
      isAuthenticated: false
    };
  },
  methods: {
  logIn(username) {
    this.isAuthenticated = username;
  },
  logOut() {
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