<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<meta name="description" content="Medidas preventivas para evitar el ciberbullying en el ámbito escolar. Información y recursos para estudiantes, docentes y padres de familia." />
<title>Medidas Preventivas para Evitar el Ciberbullying</title>
<link rel="icon" href="https://cdn-icons-png.flaticon.com/512/565/565547.png" type="image/png" />
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');
  :root {
    --color-primary: #ef036c;
    --color-secondary: #31ec56;
    --color-tertiary: #f9b872;
    --color-text: #660033;
    --color-text-light: #fce4f1;
    --color-bg: #ffe6f0;
    --color-overlay: rgba(0,0,0,0.55);
    --color-error: #cc3399;
  }
  * { box-sizing: border-box; }
  body, html {
    margin: 0; padding: 0;
    font-family: 'Poppins', sans-serif;
    background-color: var(--color-bg);
    color: var(--color-text);
    min-height: 100vh;
    overflow-x: hidden;
  }
  header {
    background: linear-gradient(90deg, var(--color-secondary), var(--color-primary));
    padding: 30px 20px;
    text-align: center;
    color: white;
    font-size: 2.8em;
    font-weight: 700;
    text-shadow: 2px 2px 6px #660033;
    letter-spacing: 1.5px;
    animation: fadeInUp 1s ease forwards;
    position: sticky;
    top: 0;
    z-index: 10;
  }
  @keyframes fadeInUp {
    from {opacity: 0; transform: translateY(30px);}
    to {opacity: 1; transform: translateY(0);}
  }
  @keyframes zoomIn {
    from {opacity: 0; transform: scale(1.1);}
    to {opacity: 1; transform: scale(1);}
  }
  /* Fondo principal: degradado rosa-verde */
  #principal {
    background: linear-gradient(135deg, #ef036c 0%, #31ec56 100%);
    min-height: 75vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
    text-shadow: 2px 2px 8px #000000cc;
    padding: 40px 20px;
    position: relative;
    overflow: hidden;
    animation: zoomIn 1.5s ease forwards;
  }
  /* Fondo estudiantes: imagen aula */
  #estudiantes {
    background-image: url('https://images.unsplash.com/photo-1503676260728-1c00da094a0b?auto=format&fit=crop&w=1470&q=80');
    background-size: cover;
    background-position: center center;
    min-height: 75vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
    text-shadow: 2px 2px 8px #000000cc;
    padding: 40px 20px;
    position: relative;
    animation: zoomIn 1.5s ease forwards;
  }
  /* Fondo padres: degradado rosa-naranja */
  #padres {
    background: linear-gradient(135deg, #ef036c 0%, #f9b872 100%);
    min-height: 75vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
    text-shadow: 2px 2px 8px #000000cc;
    padding: 40px 20px;
    position: relative;
    animation: zoomIn 1.5s ease forwards;
  }
  /* Overlay para contraste */
  .overlay {
    position: absolute;
    inset: 0;
    background: rgba(0,0,0,0.35);
    z-index: 0;
  }
  .content {
    position: relative;
    z-index: 1;
    max-width: 900px;
    text-align: center;
  }
  h1, h2 {
    margin-bottom: 20px;
    font-weight: 700;
    color: #ff99cc;
    text-shadow: 2px 2px 5px #660033cc;
  }
  h1 { font-size: 3em; }
  h2 { font-size: 2.5em; }
  p {
    font-size: 1.2em;
    line-height: 1.7em;
    color: var(--color-text-light);
    margin-bottom: 30px;
    text-shadow: 1px 1px 3px #330033cc;
  }
  .button-container, .footer-buttons {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
  }
  button {
    background: linear-gradient(135deg, var(--color-secondary), var(--color-primary));
    border: none;
    padding: 18px 40px;
    font-size: 1.2em;
    color: white;
    border-radius: 30px;
    cursor: pointer;
    box-shadow: 0 6px 15px #cc3385aa;
    transition: all 0.3s ease;
    font-weight: 700;
    letter-spacing: 0.05em;
    filter: drop-shadow(0 0 5px var(--color-secondary));
  }
  button:hover, button:focus {
    background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
    box-shadow: 0 8px 25px #cc3385dd;
    transform: translateY(-6px);
    outline: none;
  }
  .back-btn {
    cursor: pointer;
    background: var(--color-primary);
    color: white;
    padding: 10px 20px;
    border-radius: 20px;
    display: inline-block;
    margin-top: 20px;
    font-weight: 700;
    user-select: none;
    transition: background 0.3s ease;
    border: none;
    font-size: 1em;
  }
  .back-btn:hover, .back-btn:focus {
    background: var(--color-secondary);
    outline: none;
  }
  .formulario {
    background: rgba(255 230 240 / 0.9);
    padding: 25px 35px;
    border-radius: 15px;
    max-width: 600px;
    margin: 20px auto 0;
    color: var(--color-text);
    box-shadow: 0 0 20px #cc3399cc;
    text-align: left;
  }
  .formulario h3 {
    text-align: center;
    margin-bottom: 20px;
    color: #990066;
  }
  label {
    display: block;
    font-weight: 700;
    margin-top: 15px;
    color: var(--color-text);
  }
  input, textarea {
    width: 100%;
    padding: 10px;
    margin-top: 6px;
    border-radius: 8px;
    border: 1.5px solid #cc3399;
    font-size: 1em;
    resize: vertical;
    font-family: inherit;
  }
  .form-buttons {
    margin-top: 25px;
    text-align: center;
  }
  .btn-submit, .btn-cancel {
    background: var(--color-primary);
    color: white;
    border: none;
    padding: 12px 30px;
    border-radius: 25px;
    font-weight: 700;
    cursor: pointer;
    margin: 0 10px;
    box-shadow: 0 4px 10px #b32d85;
    transition: background 0.3s ease;
  }
  .btn-submit:hover, .btn-submit:focus {
    background: #b32d85;
    outline: none;
  }
  .btn-cancel {
    background: #e055a0;
  }
  .btn-cancel:hover, .btn-cancel:focus {
    background: #c13a78;
    outline: none;
  }
  .contact-info {
    background: rgba(255 240 247 / 0.9);
    padding: 20px 30px;
    border-radius: 15px;
    color: var(--color-text);
    max-width: 400px;
    margin: 30px auto 0;
    font-weight: 600;
    box-shadow: 0 0 10px #cc3399aa;
  }
  .error {
    color: var(--color-error);
    font-size: 0.9em;
    display: none;
    margin-top: 5px;
  }
  @media (max-width: 768px) {
    h1 { font-size: 2em; }
    h2 { font-size: 1.8em; }
    p, label, input, textarea, button {
      font-size: 1em;
    }
    #principal, #estudiantes, #padres, #docentes {
      min-height: 60vh;
      padding: 30px 15px;
    }
  }
</style>
</head>
<body>
<header>MEDIDAS PREVENTIVAS PARA EVITAR EL CIBERBULLYING EN EL ÁMBITO ESCOLAR</header>
<main>
  <!-- Página Principal -->
  <section id="principal" aria-label="Página principal con botones de navegación">
    <div class="overlay"></div>
    <div class="content">
      <h1>MEDIDAS PREVENTIVAS PARA EVITAR EL BULLYING EN EL ÁMBITO ESCOLAR</h1>
      <div class="button-container" role="navigation" aria-label="Navegación principal">
        <button type="button" aria-controls="estudiantes" aria-expanded="false" onclick="showSection('estudiantes', this)">Dirigida para estudiantes</button>
        <button type="button" aria-controls="docentes" aria-expanded="false" onclick="showSection('docentes', this)">Dirigida para Docentes y autoridades</button>
        <button type="button" aria-controls="padres" aria-expanded="false" onclick="showSection('padres', this)">Dirigida para padres de Familia</button>
      </div>
    </div>
  </section>
  <!-- Sección Estudiantes -->
  <section id="estudiantes" style="display:none;" aria-label="Información para estudiantes">
    <div class="overlay"></div>
    <div class="content">
      <h2>Dirigida para estudiantes</h2>
      <p>
       Concepto sobre el bullying:
El bullying es una forma de violencia sistemática que ocurre principalmente en entornos escolares, donde uno o varios estudiantes ejercen agresión física, verbal, psicológica o social hacia otro de manera intencional y repetida. Este tipo de comportamiento busca causar daño, humillación o intimidación, afectando profundamente la autoestima, el bienestar emocional y el rendimiento académico de la víctima.
Medidas de prevención dirigido especialmente a estudiantes:
La prevención del bullying comienza con el compromiso de todos los estudiantes en promover un ambiente de respeto, empatía y solidaridad. Es esencial reconocer que cada acción cuenta: evitar reírse de las burlas, no difundir rumores y no quedarse callado frente al maltrato son pasos fundamentales. Si eres testigo de una situación de acoso, no seas cómplice; apoya a quien sufre y busca la ayuda de un docente, consejero o adulto de confianza. Participar activamente en campañas escolares sobre convivencia pacífica, asistir a charlas sobre valores y trabajar en equipo con compañeros ayuda a fortalecer la unión entre estudiantes y a reducir los conflictos. Además, aprender a gestionar emociones, dialogar con respeto y aceptar las diferencias nos convierte en agentes de cambio que contribuyen a una comunidad estudiantil más justa, segura y libre de violencia.
      </p>
      <button type="button" onclick="toggleForm('formDenuncia')" class="btn-primary">Denuncia Anónima</button>
      <form id="formDenuncia" class="formulario" style="display:none;" novalidate aria-live="polite">
        <h3>Formulario de Denuncia Anónima</h3>
        <label for="descIncidente">Descripción del incidente:</label>
        <textarea id="descIncidente" name="descIncidente" rows="4" required aria-describedby="errorDesc"></textarea>
        <span class="error" id="errorDesc" aria-live="polite"></span>
        <label for="fechaIncidente">Fecha del incidente:</label>
        <input type="date" id="fechaIncidente" name="fechaIncidente" required aria-describedby="errorFecha" />
        <span class="error" id="errorFecha" aria-live="polite"></span>
        <label for="archivoIncidente">Adjuntar evidencia (opcional):</label>
        <input type="file" id="archivoIncidente" name="archivoIncidente" accept="image/*" />
        <div class="form-buttons">
          <button type="submit" class="btn-submit">Enviar denuncia</button>
          <button type="button" class="btn-cancel" onclick="toggleForm('formDenuncia')">Cancelar</button>
        </div>
      </form>
      <button type="button" class="back-btn" onclick="goHome()">Volver a Inicio</button>
    </div>
  </section>
  <!-- Sección Docentes (fondo original, sin cambios) -->
  <section id="docentes" style="display:none; background-image: url('https://images.unsplash.com/photo-1503676260728-1c00da094a0b?auto=format&fit=crop&w=1470&q=80');" aria-label="Información para docentes y autoridades">
    <div class="overlay"></div>
    <div class="content">
      <h2>Dirigida para Docentes y autoridades</h2>
      <p>
       Concepto sobre el bullying:
El bullying es una forma de violencia repetida entre estudiantes, donde uno o varios agreden intencionalmente a otro, afectando su bienestar emocional y social.
       Medidas de prevención dirigido especialmente a docentes:
Los docentes desempeñan un papel clave en la prevención y detección temprana del bullying. Es fundamental que mantengan una observación atenta y constante del comportamiento de sus estudiantes, promoviendo desde el aula una cultura de respeto, inclusión y empatía. Fomentar el diálogo, establecer normas claras de convivencia y generar espacios seguros donde cada estudiante se sienta valorado son acciones esenciales. Ante cualquier señal de acoso escolar, el docente debe actuar con prontitud, sin minimizar la situación, aplicando los protocolos establecidos por la institución y trabajando de forma coordinada con padres, autoridades escolares y personal especializado. Además, integrar la educación emocional en las actividades cotidianas permite a los estudiantes desarrollar habilidades para resolver conflictos de manera pacífica y reconocer el valor de la diversidad. El compromiso docente no solo detiene el bullying, sino que transforma el aula en un espacio de bienestar y aprendizaje integral.
      </p>
      <div class="footer-buttons">
        <button type="button" onclick="alert('Redirigiendo a Reporte de denuncias')">Reporte de denuncias</button>
        <button type="button" onclick="window.open('https://www.unicef.es/blog/como-actuar-ante-casos-de-ciberbullying-en-el-colegio', '_blank')">Medidas preventivas</button>
        <button type="button" onclick="alert('Redirigiendo a Citas agendadas')">Citas agendadas</button>
      </div>
      <button type="button" class="back-btn" onclick="goHome()">Volver a Inicio</button>
    </div>
  </section>
  <!-- Sección Padres -->
  <section id="padres" style="display:none;" aria-label="Información para padres de familia">
    <div class="overlay"></div>
    <div class="content">
      <h2>Dirigida para padres de Familia</h2>
      <p>
        Concepto sobre el bullying:
El bullying es una forma de maltrato intencional y repetido entre estudiantes, que puede ser físico, verbal o emocional, y afecta gravemente la autoestima y bienestar de los niños y adolescentes.
        Medidas de prevención dirigido especialmente a padres de familia:
Los padres juegan un papel fundamental en la prevención del bullying. Es importante mantener una comunicación abierta y constante con sus hijos, escucharlos con atención y observar cualquier cambio en su comportamiento o estado de ánimo. Fomentar en casa valores como el respeto, la empatía y la tolerancia ayuda a que los niños aprendan a convivir en armonía con los demás. También es clave enseñarles a no guardar silencio ante situaciones de acoso, ya sea que lo sufran o lo presencien, y a confiar en los adultos responsables. Estar involucrados en la vida escolar, asistir a reuniones, colaborar con los docentes y promover el diálogo con otros padres contribuye a construir una comunidad educativa unida, donde el bullying no tenga espacio.
      </p>
      <button type="button" onclick="toggleForm('formCita')" class="btn-primary">Agendar cita</button>
      <form id="formCita" class="formulario" style="display:none;" novalidate aria-live="polite">
        <h3>Formulario para Agendar Cita</h3>
        <label for="nombreCita">Nombre completo:</label>
        <input type="text" id="nombreCita" name="nombreCita" required minlength="3" aria-describedby="errorNombre" />
        <span class="error" id="errorNombre" aria-live="polite"></span>
        <label for="emailCita">Correo electrónico:</label>
        <input type="email" id="emailCita" name="emailCita" required aria-describedby="errorEmail" />
        <span class="error" id="errorEmail" aria-live="polite"></span>
        <label for="telefonoCita">Teléfono:</label>
        <input type="tel" id="telefonoCita" name="telefonoCita" pattern="^\d{7,15}$" required aria-describedby="errorTelefono" />
        <span class="error" id="errorTelefono" aria-live="polite"></span>
        <label for="motivoCita">Motivo de la cita:</label>
        <textarea id="motivoCita" name="motivoCita" rows="3" required aria-describedby="errorMotivo"></textarea>
        <span class="error" id="errorMotivo" aria-live="polite"></span>
        <label for="fechaCita">Fecha:</label>
        <input type="date" id="fechaCita" name="fechaCita" required aria-describedby="errorFechaCita" />
        <span class="error" id="errorFechaCita" aria-live="polite"></span>
        <label for="horaCita">Hora:</label>
        <input type="time" id="horaCita" name="horaCita" required aria-describedby="errorHora" />
        <span class="error" id="errorHora" aria-live="polite"></span>
        <div class="form-buttons">
          <button type="submit" class="btn-submit">Enviar solicitud</button>
          <button type="button" class="btn-cancel" onclick="toggleForm('formCita')">Cancelar</button>
        </div>
      </form>
      <button type="button" onclick="document.getElementById('contactos').style.display='block'" class="btn-primary" style="margin-top:20px;">Contactos</button>
      <div id="contactos" class="contact-info" style="display:none;" aria-live="polite">
        <p><strong>Rectorado:</strong> ########## (Situación complicada)</p>
        <p><strong>Vicerrectorado:</strong> ######### (Situación no atendida)</p>
        <p><strong>Inspección y Departamento de Consejería Estudiantil:</strong> ########## (Situación manejable)</p>
      </div>
      <button type="button" class="back-btn" onclick="goHome()">Volver a Inicio</button>
    </div>
  </section>
  <!-- Página de Agradecimiento -->
  <section id="agradecimiento" style="display:none; text-align:center; padding: 60px; color:#990066;" aria-label="Página de agradecimiento">
    <h1>AGRADECEMOS SU VISITA</h1>
    <p style="font-size: 1.3em; margin-top: 20px;">
      Esperamos haber resuelto su problema y sobre todo dar a conocer cómo se da el ciberbullying y poder a la vez prevenirlo.
    </p>
    <div class="happy-face" aria-label="Carita feliz" style="font-size: 4em; margin-top: 20px;">😊</div>
    <button type="button" class="back-btn" onclick="goHome()">Volver a Inicio</button>
  </section>
</main>
<script>
  function showSection(sectionId, btn = null) {
    const sections = document.querySelectorAll('section, #principal');
    const header = document.querySelector('header');
    const buttons = document.querySelectorAll('.button-container button');
    sections.forEach(el => el.style.display = 'none');
    header.style.display = 'none';
    if (sectionId === 'principal') {
      document.getElementById('principal').style.display = 'flex';
      header.style.display = 'block';
    } else {
      const section = document.getElementById(sectionId);
      if (section) section.style.display = 'flex';
    }
    const contactos = document.getElementById('contactos');
    if (contactos) contactos.style.display = 'none';
    buttons.forEach(button => {
      button.setAttribute('aria-expanded', 'false');
    });
    if (btn) {
      btn.setAttribute('aria-expanded', 'true');
    }
  }
  function goHome() {
    showSection('principal');
  }
  function toggleForm(id) {
    const form = document.getElementById(id);
    if (!form) return;
    if (form.style.display === 'block') {
      form.style.display = 'none';
    } else {
      form.style.display = 'block';
      form.scrollIntoView({behavior: 'smooth'});
    }
  }
  function showError(id, message) {
    const el = document.getElementById(id);
    if(el){
      el.textContent = message;
      el.style.display = 'block';
    }
  }
  function clearErrors(ids) {
    ids.forEach(id => {
      const el = document.getElementById(id);
      if(el){
        el.textContent = '';
        el.style.display = 'none';
      }
    });
  }
  function validateEmail(email) {
    const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    return re.test(email.toLowerCase());
  }
  const formDenuncia = document.getElementById('formDenuncia');
  formDenuncia.addEventListener('submit', function(e) {
    e.preventDefault();
    clearErrors(['errorDesc', 'errorFecha']);
    let valid = true;
    const desc = this.descIncidente.value.trim();
    const fecha = this.fechaIncidente.value;
    if (desc.length < 10) {
      showError('errorDesc', 'Describe el incidente con al menos 10 caracteres.');
      valid = false;
    }
    if (!fecha) {
      showError('errorFecha', 'Por favor selecciona la fecha del incidente.');
      valid = false;
    }
    if (valid) {
      alert('Denuncia enviada con éxito. Gracias por contribuir a un ambiente seguro.');
      this.reset();
      toggleForm('formDenuncia');
    }
  });
  const formCita = document.getElementById('formCita');
  formCita.addEventListener('submit', function(e) {
    e.preventDefault();
    clearErrors(['errorNombre', 'errorEmail', 'errorTelefono', 'errorMotivo', 'errorFechaCita', 'errorHora']);
    let valid = true;
    const nombre = this.nombreCita.value.trim();
    const email = this.emailCita.value.trim();
    const telefono = this.telefonoCita.value.trim();
    const motivo = this.motivoCita.value.trim();
    const fecha = this.fechaCita.value;
    const hora = this.horaCita.value;
    const today = new Date().toISOString().split('T')[0];
    if (nombre.length < 3) {
      showError('errorNombre', 'Ingresa un nombre válido (mínimo 3 caracteres).');
      valid = false;
    }
    if (!validateEmail(email)) {
      showError('errorEmail', 'Ingresa un correo electrónico válido.');
      valid = false;
    }
    if (!/^\d{7,15}$/.test(telefono)) {
      showError('errorTelefono', 'Ingresa un teléfono válido (7 a 15 dígitos).');
      valid = false;
    }
    if (motivo.length < 10) {
      showError('errorMotivo', 'Describe el motivo con al menos 10 caracteres.');
      valid = false;
    }
    if (!fecha) {
      showError('errorFechaCita', 'Selecciona la fecha de la cita.');
      valid = false;
    } else if (fecha < today) {
      showError('errorFechaCita', 'La fecha debe ser hoy o posterior.');
      valid = false;
    }
    if (!hora) {
      showError('errorHora', 'Selecciona la hora de la cita.');
      valid = false;
    }
    if (valid) {
      alert('Cita agendada correctamente. Nos pondremos en contacto pronto.');
      this.reset();
      toggleForm('formCita');
    }
  });
</script>
</body>
</html>
