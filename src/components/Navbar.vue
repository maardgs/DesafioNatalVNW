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
  justify-content: flex-start;
  gap: 10px;
  
}

img{
  width: 5.5vh;
}

p{
  font-size: 2rem;
  font-weight: 600;
  margin: 0;
  white-space: nowrap;
  
}

</style>
