<template>
  <div class="app">
    <Header />
    <nav class="navbar">
      <div class="container">
        <div class="nav-links">
          <a 
            v-for="item in navMenu" 
            :key="item.id"
            :href="item.href"
            :class="{ active: currentSection === item.id }"
            @click.prevent="scrollToSection(item.id)"
          >
            {{ item.name }}
          </a>
        </div>
      </div>
    </nav>
    
    <Home v-if="currentSection === 'home'" />
    <About v-if="currentSection === 'about'" />
    <Products v-if="currentSection === 'products'" />
    <Advantages v-if="currentSection === 'advantages'" />
    <Contact v-if="currentSection === 'contact'" />
    
    <Footer />
  </div>
</template>

<script>
import { ref } from 'vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Home from './views/Home.vue'
import About from './views/About.vue'
import Products from './views/Products.vue'
import Advantages from './views/Advantages.vue'
import Contact from './views/Contact.vue'

export default {
  components: {
    Header,
    Footer,
    Home,
    About,
    Products,
    Advantages,
    Contact
  },
  setup() {
    const currentSection = ref('home')
    const navMenu = [
      { id: 'home', name: '首页' },
      { id: 'about', name: '公司简介' },
      { id: 'advantages', name: '核心优势' },
      { id: 'products', name: '产品体系' },
      { id: 'contact', name: '联系我们' }
    ]

    const scrollToSection = (sectionId) => {
      currentSection.value = sectionId
    }

    return {
      currentSection,
      navMenu,
      scrollToSection
    }
  }
}
</script>

<style scoped>
.app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.navbar {
  background-color: #fff;
  border-bottom: 2px solid var(--light-bg);
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

.navbar .container {
  display: flex;
  justify-content: center;
}

.nav-links {
  display: flex;
  gap: 40px;
  padding: 15px 0;
  flex-wrap: wrap;
  justify-content: center;
}

.nav-links a {
  font-weight: 500;
  color: var(--secondary-color);
  border-bottom: 3px solid transparent;
  padding-bottom: 5px;
  transition: all 0.3s ease;
}

.nav-links a:hover,
.nav-links a.active {
  color: var(--primary-color);
  border-bottom-color: var(--primary-color);
}

@media (max-width: 768px) {
  .nav-links {
    gap: 20px;
    font-size: 0.9rem;
  }
}
</style>
