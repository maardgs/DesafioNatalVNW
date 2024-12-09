<script setup>
import Navbar from './Navbar.vue'
import store from '../assets/loja.png'
import Timer from './Timer.vue'
import DonationPage from './DonationPage.vue'
import Conect from './Conect.vue'
import Footer from './Footer.vue'


</script>

<template>
    <header>
        <section> 
            <div id="info">
                <Navbar />
                 <h1>Uma <span>plataforma de doação</span> para espalhar alegria</h1>
                <p>Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.</p>
                <DonationPage />
            </div>
            <img id="store" :src="store" alt="Loja de Natal">
        </section>
        <Timer />
        <Conect />
        <Footer />
    </header> 
</template>

<style scoped lang="scss">

header {
  background-color: #FFE9E8;
  height: 53vh;
  padding: 30px 0; 
}

section {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 1% 10%;

  #info {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: start;
    width: 30vw;
  }
}

h1 {
  font-size: 2rem;

  span {
    color: #CD3C32;
  } 
}

p {
  font-size: 1.2rem;
}

#store {
  width: 28vw;
}

</style>

