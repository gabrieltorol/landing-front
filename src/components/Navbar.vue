<template>
  <nav class="navbar">
    <div class="nav-container">
      <div class="nav-left">
        <router-link to="/" class="nav-logo">
          <img src="@/assets/logo-rabbit2.png" alt="RAbbit² logo" class="logo-img" />
        </router-link>
        
        <!-- Menú de hamburguesa para móviles -->
        <button class="hamburger-btn" @click="toggleMenu" :class="{ 'active': isMenuOpen }">
          <span></span>
          <span></span>
          <span></span>
        </button>
        
        <!-- Enlaces de navegación -->
        <div class="nav-links" :class="{ 'open': isMenuOpen }">
          <router-link to="/" class="nav-link" @click="closeMenu">Inicio</router-link>
          <router-link to="/soluciones" class="nav-link" @click="closeMenu">Soluciones</router-link>
          <router-link to="/capacitacion" class="nav-link" @click="closeMenu">Capacitación</router-link>
          <router-link to="/recursos" class="nav-link" @click="closeMenu">Quiénes Somos</router-link>
        </div>
      </div>
      
      <router-link to="/contacto" class="contact-btn" @click="closeMenu">Contacto</router-link>
    </div>
  </nav>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'Navbar',
  setup() {
    const isMenuOpen = ref(false)
    
    const toggleMenu = () => {
      isMenuOpen.value = !isMenuOpen.value
    }
    
    const closeMenu = () => {
      isMenuOpen.value = false
    }
    
    return {
      isMenuOpen,
      toggleMenu,
      closeMenu
    }
  }
}
</script>

<style scoped>
.navbar {
  background: linear-gradient(90deg, #591d5f 0%, #3c1d5f 100%);
  padding: 0.7rem 0;
  box-shadow: 0 2px 8px 0 rgba(0,0,0,0.10);
  position: sticky;
  top: 0;
  z-index: 100;
}

.nav-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
}

.nav-left {
  display: flex;
  align-items: center;
  gap: 2.2rem;
}

.nav-logo {
  display: flex;
  align-items: center;
  margin-right: 1.2rem;
}

.logo-img {
  height: 60px;
  vertical-align: middle;
}

.nav-link {
  color: #e0cfff;
  text-decoration: none;
  padding: 0.5rem 1.2rem;
  border-radius: 4px;
  font-size: 1.08rem;
  font-weight: 500;
  transition: background-color 0.3s, color 0.2s;
}

.nav-link:hover {
  background-color: #591d5f;
  color: #fff;
}

.nav-link.router-link-active {
  background-color: #fff;
  color: #591d5f;
  font-weight: bold;
}

.contact-btn {
  color: #fff;
  border: 1px solid #e0cfff;
  background: transparent;
  padding: 0.5rem 1.5rem;
  border-radius: 6px;
  font-size: 1.08rem;
  font-weight: 500;
  text-decoration: none;
  transition: background 0.2s, color 0.2s, border 0.2s;
  margin-left: 2rem;
}

.contact-btn:hover {
  background: #fff;
  color: #591d5f;
  border: 1px solid #fff;
}

.hamburger-btn {
  display: none; /* Hidden by default */
  flex-direction: column;
  justify-content: space-around;
  width: 24px;
  height: 20px;
  background: transparent;
  border: none;
  cursor: pointer;
  padding: 0;
  box-sizing: border-box;
}

.hamburger-btn span {
  display: block;
  width: 100%;
  height: 2px;
  background: #fff;
  border-radius: 2px;
  transition: all 0.3s ease-in-out;
}

.hamburger-btn.active span:nth-child(1) {
  transform: translateY(11px) rotate(45deg);
}

.hamburger-btn.active span:nth-child(2) {
  opacity: 0;
}

.hamburger-btn.active span:nth-child(3) {
  transform: translateY(-11px) rotate(-45deg);
}

.nav-links {
  display: flex;
  gap: 1.5rem;
  transition: transform 0.3s ease-in-out;
}

.nav-links.open {
  transform: translateY(0);
}

.nav-links.closed {
  transform: translateY(-100%);
}

@media (max-width: 900px) {
  .nav-container {
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 0 1rem;
    position: relative;
  }
  
  .nav-left {
    display: flex;
    align-items: center;
    gap: 1rem;
  }
  
  .hamburger-btn {
    display: flex;
  }
  
  .nav-links {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    flex-direction: column;
    background: linear-gradient(90deg, #591d5f 0%, #3c1d5f 100%);
    padding: 1rem 0;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    transform: translateY(-100%);
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease;
    z-index: 99;
  }
  
  .nav-links.open {
    transform: translateY(0);
    opacity: 1;
    visibility: visible;
  }
  
  .nav-link {
    padding: 0.8rem 1rem;
    border-bottom: 1px solid rgba(255,255,255,0.1);
  }
  
  .nav-link:last-child {
    border-bottom: none;
  }
  
  .contact-btn {
    margin-left: 0;
  }
}
</style> 