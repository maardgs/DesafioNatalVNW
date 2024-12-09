<script setup>
import hands from '../assets/hands.png'
import DonationPage from './DonationPage.vue'
</script>

<template>
<section> 
             <img id ="hands" :src="hands" alt="Mãos segurando um efeito de Natal">
            <div id="midle">
                <h3>Conectando generosidade ao redor do mundos</h3>
                <p>Celebre a magia do Natal de uma maneira especial! Descubra a plataforma que permite a doação de presentes 
                    significativos para aqueles que mais precisam. Faça parte do movimento e compartilhe o verdadeiro espírito da generosidade.</p>
                <DonationPage />
            </div>
        </section>
</template>

<style scoped>
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