<script setup>
import { ref } from 'vue'

const industrias = [
  {
    nombre: 'Salud',
    titulo: 'Concéntrese en la atención al paciente, no en el papeleo.',
    subtitulo: 'Reimaginar las experiencias de proveedores y pacientes.',
    imagen: '/servicios/Salud.jpeg',
    beneficios: [
      {
        titulo: 'Impulse mejores resultados para los pacientes',
        texto: 'Aumente el acceso de los pacientes a una atención de calidad y ayude a los pacientes a mantenerse encaminados hacia los resultados, apoyando la gestión de la salud de la población a escala. Además, implemente recordatorios automáticos para citas y tratamientos, y facilite la comunicación entre pacientes y profesionales de la salud para un seguimiento más efectivo.'
      },
      {
        titulo: 'Mejore el compromiso de los empleados',
        texto: 'Recupere el tiempo de su equipo para centrarse en trabajos de alto valor, como pasar tiempo con pacientes, abordar problemas complejos o investigar casos. Reclute y retenga talento de manera más efectiva. Automatice tareas administrativas repetitivas, reduzca el estrés laboral y fomente un ambiente de trabajo más productivo y satisfactorio.'
      },
      {
        titulo: 'Acelere la transformación digital',
        texto: 'Automatice los procesos mundanos, incluidos los relacionados con la gestión del ciclo de ingresos, los recursos humanos, la cadena de suministro y F&A, para que su organización pueda responder rápidamente a los cambios del mercado, los cambios de políticas y las actualizaciones normativas. Implemente soluciones digitales que permitan una adaptación ágil y eficiente a los nuevos retos del sector salud.'
      }
    ]
  },
  {
    nombre: 'Seguros',
    titulo: 'Optimice la gestión de pólizas y siniestros.',
    subtitulo: 'Transforme la experiencia de clientes y agentes.',
    imagen: '/servicios/Seguros.jpeg',
    beneficios: [
      {
        titulo: 'Procesos más ágiles',
        texto: 'Automatice la emisión de pólizas, la gestión de reclamaciones y la verificación de datos para reducir tiempos y errores. Además, integre sistemas para que la información fluya sin fricciones y mejore la eficiencia operativa en toda la compañía.'
      },
      {
        titulo: 'Mejor experiencia del cliente',
        texto: 'Ofrezca respuestas rápidas y personalizadas, mejorando la satisfacción y fidelización. Utilice chatbots y asistentes virtuales para resolver dudas y acompañar al cliente en cada etapa del proceso, generando confianza y lealtad.'
      },
      {
        titulo: 'Cumplimiento normativo',
        texto: 'Asegure la trazabilidad y el cumplimiento de regulaciones mediante flujos automatizados y reportes precisos. Mantenga registros actualizados y facilite auditorías internas y externas, minimizando riesgos regulatorios.'
      }
    ]
  },
  {
    nombre: 'Banca',
    titulo: 'Automatización segura y eficiente en banca.',
    subtitulo: 'Modernice la operación y mejore la experiencia del usuario.',
    imagen: '/servicios/Banca.jpeg',
    beneficios: [
      {
        titulo: 'Onboarding digital',
        texto: 'Agilice la apertura de cuentas y la validación de identidad con robots que verifican documentos y datos en segundos. Reduzca el tiempo de espera para nuevos clientes y mejore la seguridad en los procesos de incorporación.'
      },
      {
        titulo: 'Prevención de fraudes',
        texto: 'Implemente controles automáticos y alertas inteligentes para detectar operaciones sospechosas en tiempo real. Analice patrones de comportamiento y actúe de manera proactiva para proteger los activos de la entidad y de los clientes.'
      },
      {
        titulo: 'Gestión documental',
        texto: 'Reduzca el uso de papel y digitalice procesos internos, facilitando auditorías y consultas. Automatice la organización, almacenamiento y recuperación de documentos para una gestión más eficiente y segura.'
      }
    ]
  },
  {
    nombre: 'Servicios Públicos',
    titulo: 'Eficiencia y transparencia en servicios públicos.',
    subtitulo: 'Mejore la atención ciudadana y la gestión interna.',
    imagen: '/servicios/ServiciosPublicos.jpeg',
    beneficios: [
      {
        titulo: 'Atención 24/7',
        texto: 'Implemente bots para responder consultas y procesar solicitudes en cualquier momento. Garantice una atención continua y eficiente, mejorando la satisfacción de los ciudadanos y optimizando los recursos del organismo.'
      },
      {
        titulo: 'Procesos internos optimizados',
        texto: 'Automatice trámites, pagos y expedientes para reducir tiempos y costos. Centralice la información y facilite el seguimiento de cada gestión, asegurando transparencia y eficiencia en la administración pública.'
      },
      {
        titulo: 'Transparencia y control',
        texto: 'Genere reportes automáticos y asegure la trazabilidad de cada gestión. Permita auditorías rápidas y precisas, y cumpla con los estándares de transparencia exigidos por la normativa vigente.'
      }
    ]
  },
  {
    nombre: 'Telecomunicaciones',
    titulo: 'Agilice la gestión de clientes y servicios.',
    subtitulo: 'Reduzca tiempos de respuesta y mejore la retención.',
    imagen: '/servicios/Telecomunicaciones.jpeg',
    beneficios: [
      {
        titulo: 'Soporte automatizado',
        texto: 'Resuelva incidencias y consultas frecuentes con asistentes virtuales. Ofrezca soporte técnico inmediato y personalizado, mejorando la experiencia del usuario y reduciendo la carga del equipo humano.'
      },
      {
        titulo: 'Facturación eficiente',
        texto: 'Automatice la emisión y envío de facturas, así como la gestión de cobros. Reduzca errores y agilice los procesos de facturación, permitiendo un control financiero más preciso y transparente.'
      },
      {
        titulo: 'Análisis de datos',
        texto: 'Obtenga insights en tiempo real sobre el uso de servicios y preferencias de los clientes. Utilice estos datos para anticipar necesidades, personalizar ofertas y mejorar la toma de decisiones estratégicas.'
      }
    ]
  },
  {
    nombre: 'Manufactura',
    titulo: 'Optimice la producción y la cadena de suministro.',
    subtitulo: 'Automatización para mayor calidad y eficiencia.',
    imagen: '/servicios/Manufactura.jpeg',
    beneficios: [
      {
        titulo: 'Control de inventarios',
        texto: 'Automatice el registro y monitoreo de insumos y productos terminados. Mantenga niveles óptimos de stock, evite quiebres y reduzca pérdidas por caducidad o deterioro.'
      },
      {
        titulo: 'Mantenimiento predictivo',
        texto: 'Programe alertas y acciones automáticas para evitar paradas inesperadas. Anticipe fallas en los equipos y prolongue la vida útil de la maquinaria, reduciendo costos de reparación y tiempos de inactividad.'
      },
      {
        titulo: 'Integración de sistemas',
        texto: 'Conecte ERP, CRM y otros sistemas para un flujo de información sin errores. Mejore la coordinación entre áreas, agilice la toma de decisiones y aumente la eficiencia operativa en toda la planta.'
      }
    ]
  }
]

const industriaSeleccionada = ref(0)
const dropdownAbierto = ref(true)
</script>

<template>
  <div class="soluciones-bg">
    <h1 class="soluciones-title">¿Cómo usar RPA + IA en tu industria?</h1>
    
    <div class="soluciones-container">     <!-- Dropdown lateral -->
      <div class="soluciones-sidebar">
        <div class="dropdown-container">
          <button 
            class="dropdown-button"
            @click="dropdownAbierto = !dropdownAbierto"
          >
            <span>{{ industrias[industriaSeleccionada].nombre }}</span>
            <svg class="dropdown-icon" :class="{ 'rotated': dropdownAbierto }" fill="none" stroke="currentColor" viewBox="0 0 24 24">             <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
            </svg>
          </button>
          
          <div class="dropdown-menu" :class="{ open: dropdownAbierto }">
            <div
              v-for="(industria, idx) in industrias"
              :key="industria.nombre"
              :class="['dropdown-item', { active: industriaSeleccionada === idx }]"
              @click="() => { industriaSeleccionada = idx;}"
            >
              {{ industria.nombre }}
            </div>
          </div>
        </div>
      </div>
      
      <!-- Contenido principal -->
      <div class="soluciones-content">       <!-- Imagen al inicio -->
        <div class="soluciones-header-image">
          <img 
            :src="industrias[industriaSeleccionada].imagen" 
            :alt="industrias[industriaSeleccionada].nombre"
            class="industria-imagen"
          />
        </div>
        
        <div class="soluciones-header">
          <div class="soluciones-header-text">         <h2 class="soluciones-content-title">{{ industrias[industriaSeleccionada].titulo }}</h2>
            <p class="soluciones-content-subtitle">{{ industrias[industriaSeleccionada].subtitulo }}</p>
          </div>
        </div>
        
        <div class="soluciones-beneficios">
          <ul class="beneficios-lista">
            <li v-for="(beneficio, i) in industrias[industriaSeleccionada].beneficios" :key="i" class="beneficio-item">              <div class="beneficio-check">
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/>
                </svg>
              </div>
              <div class="beneficio-content">
                <h4 class="beneficio-title">{{ beneficio.titulo }}</h4>
                <p class="beneficio-text">{{ beneficio.texto }}</p>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
  <!-- Call to Action eliminado por solicitud del usuario -->
</template>

<style scoped>
.soluciones-bg {
  min-height: 100vh;
  background: #181028;
  padding: 0 0 4rem 0;
}
.soluciones-title {
  text-align: center;
  font-size: 2.5rem;
  font-weight: 800;
  margin: 0 0 2.5rem 0;
  letter-spacing: 1px;
  color: #fff;
  padding-top: 2.5rem;
}

.soluciones-container {
  display: flex;
  max-width: 1400px;
  margin: 0 auto;
  gap: 3rem;
  padding: 0 2rem;
}

/* Sidebar con dropdown */
.soluciones-sidebar {
  flex: 0 0 300px;
  position: sticky;
  top: 2rem;
  height: fit-content;
}

.dropdown-container {
  position: relative;
  width: 100%;
}

.dropdown-button {
  width: 100%;
  padding: 1rem 1.5rem;
  background: linear-gradient(90deg, #7c3aed 0%, #a21caf 100%);
  color: #fff;
  border: none;
  border-radius: 12px;
  font-size: 1.1rem;
  font-weight: 600;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: space-between;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(124, 58, 237, 0.3);
}

.dropdown-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(124, 58, 237, 0.4);
}

.dropdown-icon {
  width: 20px;
  height: 20px;
  transition: transform 0.3s ease;
}

.dropdown-icon.rotated {
  transform: rotate(180deg);
}

.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  right: 0;
  background: #231130;
  border: 1px solid #7c3aed;
  border-radius: 12px;
  margin-top: 0.5rem;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
  z-index: 1000;
  visibility: hidden;
  transform: translateY(-10px);
  transition: all 0.3s ease;
  max-height: 0;
  overflow: hidden;
}

.dropdown-menu.open {
  opacity: 1;
  visibility: visible;
  transform: translateY(0);
  max-height: 400px; /* Adjust as needed */
}

.dropdown-item {
  padding: 1rem 1.5rem;
  color: #e0cfff;
  cursor: pointer;
  transition: all 0.2s ease;
  border-bottom: 1px solid rgba(124, 58, 237, 0.2);
}

.dropdown-item:last-child {
  border-bottom: none;
}

.dropdown-item:hover {
  background: rgba(124, 58, 237, 0.2);
  color: #fff;
}

.dropdown-item.active {
  background: rgba(124, 58, 237, 0.3);
  color: #fff;
  font-weight: 600;
}

/* Contenido principal */
.soluciones-content {
  flex: 1;
  padding: 2rem;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 20px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
}

.soluciones-header {
  display: flex;
  align-items: center;
  gap: 2rem;
  margin-bottom: 3rem;
  padding-bottom: 2rem;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.soluciones-header-text {
  flex: 1;
}

.soluciones-header-image {
  width: 100%;
  height: 320px;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
  margin: 0 auto 2rem auto;
  display: flex;
  align-items: center;
  justify-content: center;
}
.industria-imagen {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.industria-imagen:hover {
  transform: scale(1.05);
}

.soluciones-content-title {
  font-size: 2.2rem;
  font-weight: 700;
  color: #fff;
  margin-bottom: 1rem;
  line-height: 1.2;
}
.soluciones-content-subtitle {
  font-size: 1.2rem;
  color: #e0cfff;
  margin-bottom: 2.5rem;
  line-height: 1.4;
}

.soluciones-beneficios {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.beneficio-card {
  background: linear-gradient(135deg, rgba(124, 58, 237, 0.1) 0%, rgba(162, 28, 175, 1) 100%);
  border: 1px solid rgba(124, 58, 237, 0.3);
  border-radius: 16px;
  padding: 2rem;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.beneficio-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, #7c3aed 0%, #a21caf 100%);
  transform: scaleX(0);
  transition: transform 0.3s ease;
}

.beneficio-card:hover::before {
  transform: scaleX(1);
}

.beneficio-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 30px rgba(124, 58, 237, 0.3);
  border-color: rgba(124, 58, 237, 0.5);
}

.beneficio-icon {
  width: 50px;
  height: 50px;
  background: linear-gradient(135deg, #7c3aed 0%, #a21caf 100%);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
  color: #fff;
}

.beneficio-icon svg {
  width: 24px;
  height: 24px;
}

.beneficio-content {
  position: relative;
  z-index: 1;
}

.beneficio-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: #fff;
  margin-bottom: 0.3rem;
  line-height: 1.3;
}
.beneficio-text {
  color: #e0cfff;
  line-height: 1.5;
  font-size: 0.98rem;
}

/* NUEVOS ESTILOS PARA BULLETPOINTS Y AJUSTE DE IMAGEN */
.beneficios-titulo {
  color: #fff;
  font-size: 1.3rem;
  font-weight: 700;
  margin-bottom: 1.2rem;
}
.beneficios-lista {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}
.beneficio-item {
  display: flex;
  align-items: flex-start;
  background: linear-gradient(135deg, rgba(124, 58, 237, 0.08) 0%, rgba(162, 28, 175, 0.18) 100%);
  border-radius: 14px;
  padding: 1.2rem 1.5rem;
  box-shadow: 0 2px 10px rgba(124, 58, 237, 0.08);
  border: 1px solid rgba(124, 58, 237, 0.18);
}
.beneficio-check {
  min-width: 36px;
  height: 36px;
  background: linear-gradient(135deg, #7c3aed 0%, #a21caf 100%);
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 1.2rem;
  color: #fff;
  box-shadow: 0 2px 8px rgba(124, 58, 237, 0.15);
}
.beneficio-check svg {
  width: 20px;
  height: 20px;
}
.beneficio-content {
  flex: 1;
}
.beneficio-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: #fff;
  margin-bottom: 0.3rem;
  line-height: 1.3;
}
.beneficio-text {
  color: #e0cfff;
  line-height: 1.5;
  font-size: 0.98rem;
}

/* Responsive */
@media (max-width: 768px) {
  .soluciones-container {
    flex-direction: column;
    gap: 2rem;
  }
  
  .soluciones-sidebar {
    flex: none;
    position: static;
  }
  
  .soluciones-content {
    padding: 1.5rem;
  }
  
  .soluciones-header {
    flex-direction: column;
    text-align: center;
    gap: 1.5rem;
  }
  
  .soluciones-header-image {
    flex: 0 0 150px;
    width: 100%;
    max-width: 300px;
  }
  
  .soluciones-content-title {
    font-size: 1.8rem;
  }
  
  .soluciones-beneficios {
    grid-template-columns: 1fr;
  }
  
  .beneficio-card {
    padding: 1.5rem;
  }
}

@media (max-width: 480px) {
  .soluciones-title {
    font-size: 2rem;
    padding: 1.5rem 1em 0rem;
  }
  
  .soluciones-container {
    padding: 0 1rem;
  }
  
  .beneficio-title {
    font-size: 1.2rem;
  }
}
</style> 