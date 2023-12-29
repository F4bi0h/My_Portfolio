<template>
  <div id="app">
    <video autoplay muted loop>
      <source src="./assets/bg-video.mp4">
    </video>
    <transition name="slide-fade">
      <div>
        <PortfolioHome />
        <PortfolioSection />
      </div>
    </transition>
  </div>
</template>

<script>
import PortfolioHome from './components/PortfolioHome.vue';
import PortfolioSection from './components/PortfolioSection.vue';

export default {
  name: 'App',
  data() {
    return {
      show: false
    }
  },
  components: {
    PortfolioHome,
    PortfolioSection
  }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Kanit:wght@300&display=swap');

#app {
  font-family: 'Kanit';
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  overflow: hidden;
  background: #000;
  overflow-y: hidden;
}

#app video {
  position: fixed;
  top: 0;
  left: 0;
  object-fit: cover;
  width: 100%;
  opacity: 0;
  animation: fade-in 3s normal forwards ease-in-out;
}

@keyframes fade-in {
  from {
    opacity: 0;
  }

  to {
    opacity: 1;
  }
}
</style>
