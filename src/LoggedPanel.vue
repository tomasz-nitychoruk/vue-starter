<template>
   <div>
       <h2>Witaj {{ username }}</h2>
        <a @click="logOut()">Wyloguj się</a>
   </div>
</template>

<script>
export default {
    props: ['username'],
 
 methods: {
     logOut() {
         this.$emit('logout');
     }
 }
}
</script>