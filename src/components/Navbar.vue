<script setup>
import noel from '../assets/noel.png'
</script>

<template>
  <section> 
  <div id="navbar"> 
  <img :src="noel" alt="Noel"> 
  <p>Feliz Natal</p>
  </div>
  </section>
</template>

<style scoped lang = "scss">

#navbar{
  display: flex;
  align-items: center;
  justify-content: center;
}

img{
  width: 5.5vh;
}

p{
  font-size: 1.5rem;
  font-weight: 600;
  margin: 7%;
  width: 150px;
}

</style>
