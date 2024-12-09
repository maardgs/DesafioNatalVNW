<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import presentes from "../assets/gifts.png";

const days = ref("00");
const hours = ref("00");
const minutes = ref("00");
const seconds = ref("00");

function calculateTime() {
  const now = new Date();
  const christmas = new Date(now.getFullYear(), 11, 25);
  const timeDifference = christmas - now;

  if (timeDifference <= 0) {
    days.value = "00";
    hours.value = "00";
    minutes.value = "00";
    seconds.value = "00";
    return;
  }

  const d = Math.floor(timeDifference / (1000 * 60 * 60 * 24));
  const h = Math.floor((timeDifference / (1000 * 60 * 60)) % 24);
  const m = Math.floor((timeDifference / (1000 * 60)) % 60);
  const s = Math.floor((timeDifference / 1000) % 60);

  days.value = d.toString().padStart(2, "0");
  hours.value = h.toString().padStart(2, "0");
  minutes.value = m.toString().padStart(2, "0");
  seconds.value = s.toString().padStart(2, "0");
}

let timerInterval;
onMounted(() => {
  calculateTime();
  timerInterval = setInterval(calculateTime, 1000);
});

onUnmounted(() => {
  clearInterval(timerInterval);
});
</script>

<template>
  <section>
    <div id="timer">
      <h2>Tempo limitado</h2>
      <p>Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.</p>
    <h3>
      {{ days }}d - {{ hours }}h - {{ minutes }}m - {{ seconds }}s
    </h3>
    <img :src="presentes" alt="caixas de presente" />    
    </div>
    
  </section>
</template>

<style scoped>

section {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

#timer {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin-bottom: 2rem;
  padding: 5rem 8rem 0 8rem;
}

h2 {
  font-weight: 600;
  font-size: 2rem;
}

p {
  font-size: 1.1rem;
  max-width: 70%;
  margin: 1rem 0 2rem;
}

h3 {
  font-size: 3rem;
  color: #cd3c32;
  margin-bottom: 2rem;
}


img {
  width: 30vw;
  margin: 3vh 0 8vh;
}
</style>
