<template>
  <header>
    <img src="/logo.jpg" alt="Logo">
    
    <NavButton 
      v-for="section in sections"
      :key="section.name"
      :section-name="section.name"
      :display-label="section.label"
      :is-active="currentSection === section.name"
      @navigate="goToSection"
    />
  </header>

  <main class="content-area">
    <section :id="currentSection" class="active">
      <Muro v-if="currentSection === 'muro'" />
      <Info v-else-if="currentSection === 'info'" />
      <Photos v-else-if="currentSection === 'photos'" />
      <Boxes v-else-if="currentSection === 'boxes'" />
    </section>
  </main>
</template>

<script>
import { ref, onMounted, onUnmounted } from 'vue';
import NavButton from './components/NavButton.vue';
import Muro from './components/Muro.vue';
import Info from './components/Info.vue';
import Photos from './components/Photos.vue';
import Boxes from './components/Boxes.vue';

export default {
  name: 'App',
  components: {
    NavButton,
    Muro,
    Info,
    Photos,
    Boxes
  },
  setup() {
    const sections = [
      { name: 'muro', label: 'Muro' },
      { name: 'info', label: 'Info' },
      { name: 'photos', label: 'Photos' },
      { name: 'boxes', label: 'Boxes' }
    ];

    const currentSection = ref('muro');


    const goToSection = (section) => {
      currentSection.value = section;

      if (location.hash !== '#' + section) {
        history.pushState(null, '', '#' + section);
      }
    };

    const handlePopState = () => {
      const sec = location.hash.replace('#', '') || 'muro';
      goToSection(sec);
    };

    onMounted(() => {
      const initial = location.hash.replace('#', '') || 'muro';
      goToSection(initial);
      
      window.addEventListener('popstate', handlePopState);
    });


    onUnmounted(() => {
      window.removeEventListener('popstate', handlePopState);
    });

    return {
      sections,
      currentSection,
      goToSection
    };
  }
}
</script>

<style scoped>
/* 🔴 COPIA COMPLETA DEL CSS ORIGINAL MIGRADO */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  background: #f2f2f2;
}




header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: #3b5998; 
  color: white;
  padding: 10px;
}

img{
    width: 40%;
    height: 40%;
}

input{
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 20px;
    height: 40px;
}

button header {
  display: flex;
  justify-content: center;
  align-items: center;
}


#foto1{
    height: 300px;
}

#foto2{ 
    height: 100px;
    width: 100px;
}

button {
  background: white; 
  color: #4267B2;
  border: none;
  padding: 8px 12px;
  border-radius: 4px;
  cursor: pointer;
}


.nav-btn.active {
    background: #4a6fa8; 
    color: white;
}

/* Estilos de las secciones */
main section {
  background: white;
  padding: 15px;
  border-radius: 6px;
  margin-bottom: 10px;
}

</style>