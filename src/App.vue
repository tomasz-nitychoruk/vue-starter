<template>
  <div>
    <h1>Twój e-mail to: {{ email }}</h1>
    
<div v-id="email.length > 0">
  <div v-if="email.length < 10">Ale masz krótki adres!</div>
<div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
<div v-else class="red">Twój adres e-mail jest stanowczo za długi.</div>
</div>

    <input type="email" v-model="email">
    
  </div>

</template>

<script>
export default {
  data() {
    return {
      email: "",
      password: ""
    };
  }
}
</script>

<style>
.red{
  color:red;
}
</style>
