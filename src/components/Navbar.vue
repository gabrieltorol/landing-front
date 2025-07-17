<template>
  <nav class="navbar">
    <div class="nav-container">
      <div class="nav-left">
        <router-link to="/" class="nav-logo">
          <img src="@/assets/logo-rabbit2.png" alt="Rabbit2 logo" class="logo-img" />
        </router-link>
        <router-link to="/" class="nav-link">Inicio</router-link>
        <router-link to="/soluciones" class="nav-link">Soluciones</router-link>
        <router-link to="/capacitacion" class="nav-link">Capacitación</router-link>
        <router-link to="/recursos" class="nav-link">Recursos</router-link>
      </div>
      <router-link to="/contacto" class="contact-btn">Contacto</router-link>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
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

@media (max-width: 900px) {
  .nav-container {
    flex-direction: column;
    gap: 0.7rem;
    padding: 0 1rem;
  }
  .nav-left {
    flex-direction: column;
    gap: 1rem;
  }
  .contact-btn {
    margin-left: 0;
  }
}
</style> 