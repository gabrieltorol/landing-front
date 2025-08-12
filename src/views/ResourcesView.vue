<template>
  <div class="quienes-somos-bg">
    <!-- Título principal -->
    <section class="hero-section">
      <h1 class="hero-title">El Potencial Oculto. La Transformación en Acción.</h1>
    </section>

    <!-- El Problema Universal y la Revelación -->
    <section class="problema-section">
      <div class="content-container">
        <p class="problema-text">
          Durante años, observábamos la misma paradoja en casi todas las organizaciones: tecnología de punta utilizada apenas en un bajo porcentaje, y un enorme potencial humano desaprovechado. La respuesta, descubrimos, no estaba en el siguiente software, sino en un cambio cultural.
        </p>
        <p class="problema-text">
          Nuestra revelación no llegó en una sala de reuniones, sino en la práctica, formando equipos que muchos creían imposibles. Vimos a un Gerente de Planta y un analista de RR.HH. diseñar juntos, en una célula ágil, una solución para sus propios desafíos. Vimos a contadores y vendedores construir bots para automatizar las tareas que los consumían a diario.
        </p>
        <p class="problema-text">
          Comprendimos que cuando se empodera a las personas que conocen el problema, con las herramientas adecuadas y una metodología ágil, la transformación no es una meta lejana. Es un resultado inevitable.
        </p>
      </div>
    </section>

    <!-- Presentación de la Marca -->
    <section class="marca-section">
      <div class="content-container">
        <h2 class="marca-title">De esa convicción nace RAbbit²</h2>
        <p class="marca-text">
          Somos el socio estratégico que destapa el potencial oculto en tu empresa. Creemos que la verdadera agilidad, esa que genera un crecimiento exponencial, nace de la sinergia de la experiencia, potenciada al cuadrado.
        </p>
      </div>
    </section>

    <!-- Los Fundadores -->
    <section class="fundadores-section">
      <div class="content-container">
        <h2 class="fundadores-title">Nuestra fundación es la unión de tres visiones, forjadas para resolver este desafío.</h2>
        
        <div class="fundadores-grid">
          <div class="fundador-card">
            <div class="fundador-header">
              <h3 class="fundador-nombre">Iván Cabrera</h3>
              <p class="fundador-cargo">Chief Executive Officer, Co-Founder</p>
            </div>
            <p class="fundador-descripcion">
              Como CEO, Iván es el responsable de definir la visión estratégica y el crecimiento de RAbbit². Su misión es posicionar a la compañía como el socio clave para la transformación digital, asegurando que cada solución de RPA o Inteligencia Artificial estén perfectamente alineadas con los objetivos del negocio y, sobre todo, con la cultura y las personas que lo impulsan.
            </p>
          </div>

          <div class="fundador-card">
            <div class="fundador-header">
              <h3 class="fundador-nombre">Francisco Novello</h3>
              <p class="fundador-cargo">Chief Operating Officer, Co-Founder</p>
            </div>
            <p class="fundador-descripcion">
              Como COO, Francisco es el arquitecto de la excelencia operativa de RAbbit². Su responsabilidad es asegurar que cada proyecto se ejecute con precisión y eficiencia, traduciendo la visión estratégica en soluciones robustas y seguras que entregan resultados tangibles y medibles para nuestros clientes.
            </p>
          </div>

          <div class="fundador-card">
            <div class="fundador-header">
              <h3 class="fundador-nombre">Danilo Toro</h3>
              <p class="fundador-cargo">Chief Technology Officer, Co-Founder</p>
            </div>
            <p class="fundador-descripcion">
              Como CTO, Danilo es el motor de la innovación y la excelencia técnica. Su principal enfoque es definir la estrategia tecnológica que mantiene a RAbbit² a la vanguardia, aportando las herramientas de automatización e IA que, en manos de los equipos de nuestros clientes, abren las puertas a una eficiencia antes inimaginable.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- La Promesa -->
    <section class="promesa-section">
      <div class="content-container">
        <h2 class="promesa-title">La Promesa</h2>
        <p class="promesa-text">
          En RAbbit², nuestra misión es clara: liberar el talento humano para lo que ninguna máquina podrá hacer: pensar, colaborar, crear e innovar.
        </p>
        <p class="promesa-text">
          No solo implementamos soluciones; construimos puentes y formamos a tus equipos para que ellos mismos se conviertan en el motor del cambio.
        </p>
        <p class="promesa-text">
          Co-creamos su nuevo ADN Digital para ayudar a su empresa a dar, juntos, el gran salto.
        </p>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'QuienesSomosView'
}
</script>

<style scoped>
.quienes-somos-bg {
  min-height: 100vh;
  background: transparent;
  padding-bottom: 4rem;
}

.content-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

/* Hero Section */
.hero-section {
  text-align: center;
  padding: 6rem 0 4rem 0;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 900;
  color: #fff;
  margin: 0;
  line-height: 1.2;
  letter-spacing: 1px;
}

/* Problema Section */
.problema-section {
  padding: 4rem 0;
  background: rgba(124, 58, 237, 0.05);
  margin: 2rem 0;
}

.problema-text {
  font-size: 1.25rem;
  color: #e0cfff;
  line-height: 1.8;
  margin-bottom: 2rem;
  text-align: justify;
}

.problema-text:last-child {
  margin-bottom: 0;
}

/* Marca Section */
.marca-section {
  padding: 4rem 0;
  text-align: center;
}

.marca-title {
  font-size: 2.5rem;
  font-weight: 800;
  color: #fff;
  margin-bottom: 2rem;
}

.marca-text {
  font-size: 1.3rem;
  color: #e0cfff;
  line-height: 1.7;
  max-width: 800px;
  margin: 0 auto;
}

/* Fundadores Section */
.fundadores-section {
  padding: 4rem 0;
  background: rgba(124, 58, 237, 0.05);
  margin: 2rem 0;
}

.fundadores-title {
  font-size: 2.2rem;
  font-weight: 800;
  color: #fff;
  text-align: center;
  margin-bottom: 3rem;
  max-width: 900px;
  margin-left: auto;
  margin-right: auto;
}

.fundadores-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2.5rem;
  margin-top: 3rem;
}

.fundador-card {
  background: rgba(124, 58, 237, 0.1);
  border-radius: 20px;
  padding: 2.5rem;
  border: 1px solid rgba(124, 58, 237, 0.2);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.fundador-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(124, 58, 237, 0.2);
}

.fundador-header {
  margin-bottom: 1.5rem;
  text-align: center;
}

.fundador-nombre {
  font-size: 1.5rem;
  font-weight: 800;
  color: #fff;
  margin: 0 0 0.5rem 0;
}

.fundador-cargo {
  font-size: 1.1rem;
  color: #a21caf;
  font-weight: 600;
  margin: 0;
}

.fundador-descripcion {
  font-size: 1.1rem;
  color: #e0cfff;
  line-height: 1.7;
  text-align: justify;
  margin: 0;
}

/* Promesa Section */
.promesa-section {
  padding: 4rem 0;
  text-align: center;
}

.promesa-title {
  font-size: 2.5rem;
  font-weight: 800;
  color: #fff;
  margin-bottom: 2.5rem;
}

.promesa-text {
  font-size: 1.3rem;
  color: #e0cfff;
  line-height: 1.8;
  margin-bottom: 2rem;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

.promesa-text:last-child {
  margin-bottom: 0;
}

/* Responsive Design */
@media (max-width: 768px) {
  .hero-title {
    font-size: 2.5rem;
  }
  
  .content-container {
    padding: 0 1rem;
  }
  
  .fundadores-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  
  .fundador-card {
    padding: 2rem;
  }
  
  .marca-title,
  .fundadores-title,
  .promesa-title {
    font-size: 2rem;
  }
  
  .problema-text,
  .marca-text,
  .promesa-text {
    font-size: 1.1rem;
  }
}
</style> 