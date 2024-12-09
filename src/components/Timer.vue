<script setup>
import presentes from '../assets/gifts.png'
</script>

<template>
  <section>
    <div>
      <h2>Tempo limitado</h2>
      <p>Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.</p>
    </div>

    <h3 id="cronometro">16d -5h - 01m  - 36s</h3>

    <img :src="presentes" alt="">
  </section>

</template>

<style scoped>
section {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  div {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: column;
    height: 10vh;
    margin: 8vh 0 3vh;

    h2 {
      font-weight: 600;
      font-size: 3rem;
    }
    p {
      font-size: 1.4rem;
      width: 60%;
      text-align: center;
    }
  }

  h3 {
    font-size: 5rem;
    color: #CD3C32;
  }

  img { 
    width: 20vw; 
    margin: 3vh 0 8vh;
  }

</style>
