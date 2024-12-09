<script setup>
import noel from '../assets/noel.png'
import logo_facebook from '../assets/logo_facebook.png'
import logo_instagram from '../assets/logo_instagram.png'
import logo_twitter from '../assets/logo_twitter.png'
import logo_whatsapp from '../assets/logo-whatsapp.png'
import logo_google from '../assets/logo_google.png'
</script>

<template>
<section id="footer">
  <div> 
  <img :src="noel" alt="Noel"> 
  <p>Feliz Natal</p>
  </div>
  <div id="icons">
    <img :src="logo_twitter" alt="Twitter">
    <img :src="logo_whatsapp" alt="Whatsapp">
    <img :src="logo_instagram" alt="Instagram">
    <img :src="logo_facebook" alt="Facebook">
    <img :src="logo_google" alt="Google">
  </div>
  </section>
</template>

<style scoped>
#footer {
  background-color: #ffd5d3;
  height: 190px; 
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 5%; 
}

img {
  width: 40px;
  &:hover {
    cursor: pointer;
  } 
}

p {
  font-size: 1.5rem;
  font-weight: 600;
  margin: 0;
}

#icons {
  display: flex;
  gap: 10px; 
  background-color: #ffd5d3;
  
  &:hover {
    cursor: pointer;
  }
}
</style>