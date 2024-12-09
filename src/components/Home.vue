<script setup>
import Navbar from './Navbar.vue'
import Timer from './Timer.vue'
import DonationPage from './DonationPage.vue'
import store from '../assets/loja.png' 
import hands from '../assets/hands.png'
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
        <section> 
             <img id ="hands" :src="hands" alt="Mãos segurando um efeito de Natal">
            <div id="midle">
                <h3>Conectando generosidade ao redor do mundos</h3>
                <p>Celebre a magia do Natal de uma maneira especial! Descubra a plataforma que permite a doação de presentes 
                    significativos para aqueles que mais precisam. Faça parte do movimento e compartilhe o verdadeiro espírito da generosidade.</p>
                <DonationPage />
            </div>
        </section>
        <Footer />
    </header> 
</template>

<style scoped lang="scss">

header {
  background-color: #FFE9E8;
  height: 53vh;
}

section {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5% 15%;

  #info {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: start;
    width: 29vw;
  }
}

h1 {
  font-size: 3rem;

  span {
    color: #CD3C32;
  } 
}

p {
  font-size: 1.6rem;
}

#store {
  width: 28vw;
}

#midle {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: start;
    width: 29vw;
    

}
#hands{
    width: 28vw;
}

h3 {
  font-weight: 600;
  font-size: 3rem;
  
  p{
    font-size: 1.4rem;
      width: 60%;
      margin-bottom: 1.5rem;
      
  }
}

</style>

