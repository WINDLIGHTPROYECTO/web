<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Windlight - Iluminación Eólica Inteligente</title>
  <style>
    /* ============================
       RESET BÁSICO
    ============================ */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f9f9f9;
      color: #333;
      line-height: 1.6;
      scroll-behavior: smooth;
    }
    /* ============================
       ENCABEZADO
    ============================ */
    header {
      background: url("https://th.bing.com/th/id/OIP.yvuqLdXqFPmsrUP1SgfezgHaE8?w=262&h=180&c=7&r=0&o=5&pid=1.7") no-repeat center center;
      background-size: cover;
      height: 60vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: #fff;
      position: relative;
    }
    header::after {
      content: "";
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.4);
    }
    header h1 {
      font-size: 3.5em;
      z-index: 1;
      text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.6);
      transition: transform 0.5s ease;
    }
    header h1:hover {
      transform: scale(1.05);
    }
    /*  
       NAVEGACIÓN
    ============================ */
    nav {
      background: #004080;
      padding: 10px 0;
      display: flex;
      justify-content: center;
      position: sticky;
      top: 0;
      z-index: 2;
    }
    nav a {
      color: #fff;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
      transition:  0.3s ease, transform 0.3s ease;
      padding: 8px 12px;
      border-radius: 4px;
    }
    nav a:hover {
      background: #0059b3;
      transform: translateY(-3px);
    }
    /* ============================
       CONTENEDOR GENERAL
    ============================ */
    .container {
      max-width: 1200px;
      margin: 30px auto;
      padding: 0 20px;
    }
    .container h2 {
      margin-bottom: 15px;
      color: #004080;
      font-size: 2em;
      text-align: center;
    }
    .container p {
      margin-bottom: 15px;
      text-align: justify;
    }
    section {
      margin-bottom: 40px;
      opacity: 0;
      transform: translateY(20px);
      animation: fadeInUp 0.8s forwards;
    }
    section:nth-child(odd) {
      animation-delay: 0.2s;
    }
    section:nth-child(even) {
      animation-delay: 0.4s;
    }
    @keyframes fadeInUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    /* ============================
       VENTAJAS Y DESVENTAJAS
    ============================ */
    .advantages-disadvantages {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      margin-top: 20px;
      justify-content: center;
    }
    .advantages, .disadvantages {
      flex: 1 1 45%;
      background: #fff;
      border: 1px solid #ddd;
      border-radius: 8px;
      padding: 20px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .advantages:hover, .disadvantages:hover {
      transform: translateY(-5px);
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
    }
    .advantages h3, .disadvantages h3 {
      margin-bottom: 10px;
      color: #004080;
      text-align: center;
    }
    ul {
      list-style: disc inside;
      margin-left: 20px;
      margin-top: 10px;
    }
    /* ============================
       EQUIPO (INTEGRANTES Y FUNCIONES)
    ============================ */
    .team {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }
    .member {
      flex: 1 1 250px;
      background: #fff;
      border: 1px solid #ddd;
      border-radius: 8px;
      padding: 20px;
      text-align: center;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .member:hover {
      transform: translateY(-5px);
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
    }
    .member img {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 10px;
      transition: transform 0.3s ease;
    }
    .member img:hover {
      transform: scale(1.1);
    }
    .member h4 {
      margin-bottom: 5px;
      color: #004080;
    }
    .member p {
      font-size: 0.9em;
    }
    /* ============================
       GALERÍA DE IMÁGENES
    ============================ */
    .gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }
    .gallery img {
      width: 300px;
      border-radius: 8px;
      border: 1px solid #ccc;
      object-fit: cover;
      transition: transform 0.4s ease, filter 0.4s ease;
      cursor: pointer;
    }
    .gallery img:hover {
      transform: scale(1.05);
      filter: brightness(1.1);
    }
    /* ============================
       PIE DE PÁGINA
    ============================ */
    footer {
      background: #004080;
      color: #fff;
      text-align: center;
      padding: 20px 0;
      margin-top: 40px;
    }
  </style>
</head>
<body>
  <!-- ENCABEZADO -->
  <header>
    <h1>WINDLIGHT</h1>
  </header>
  <!-- NAVEGACIÓN -->
  <nav>
    <a href="#descripcion">Descripción</a>
    <a href="#objetivos">Objetivos</a>
    <a href="#ventajas-desventajas">Ventajas y Desventajas</a>
    <a href="#equipo">Equipo</a>
    <a href="#aplicacion">Aplicación</a>
    <a href="#conclusion">Conclusiones</a>
    <a href="#anexos">Anexos</a>
  </nav>
  <!-- CONTENEDOR GENERAL -->
  <div class="container">
    <!-- DESCRIPCIÓN DEL PROYECTO -->
    <section id="descripcion">
      <h2>Descripción del Proyecto</h2>
      <p>
        <strong>Windlight</strong> es un sistema de <em>iluminación eólica inteligente</em> diseñado para ser autosustentable. Utiliza una turbina de viento para generar electricidad, la cual se gestiona mediante un microcontrolador Arduino. El sistema permite monitorear en tiempo real el consumo eléctrico a través de sensores de corriente, optimizando así el uso de la energía.
      </p>
      <p>
        Con Windlight buscamos fomentar la <strong>eficiencia energética</strong> y la <strong>conciencia ambiental</strong>, aprovechando la fuerza del viento para iluminar espacios de manera limpia y sostenible.
      </p>
      <p style="text-align:center;">
        <img src="https://th.bing.com/th/id/OIP.CPEU78wgQy1_MOleFxiIfQHaFP?rs=1&pid=ImgDetMain" alt="Turbina eólica" style="max-width:80%; border-radius: 8px;">
      </p>
    </section>
    <!-- OBJETIVOS -->
    <section id="objetivos">
      <h2>Objetivos</h2>
      <p>
        Nuestro propósito es reducir el impacto ambiental mediante la implementación de sistemas de iluminación basados en energías renovables y controlados inteligentemente.
      </p>
      <h3>Objetivo General</h3>
      <p>
        Diseñar y desarrollar un sistema de iluminación autosustentable con Arduino, aprovechando la energía generada por la turbina eólica y monitoreando el consumo en tiempo real.
      </p>
      <h3>Objetivos Específicos</h3>
      <ul>
        <li>Instalar y configurar una turbina eólica de bajo costo.</li>
        <li>Implementar un sistema de monitoreo mediante sensores de corriente.</li>
        <li>Desarrollar un algoritmo para optimizar el consumo energético.</li>
        <li>Evaluar la viabilidad económica y el impacto ambiental.</li>
      </ul>
    </section>
    <!-- VENTAJAS Y DESVENTAJAS -->
    <section id="ventajas-desventajas">
      <h2>Ventajas y Desventajas</h2>
      <div class="advantages-disadvantages">
        <div class="advantages">
          <h3>Ventajas</h3>
          <ul>
            <li>Energía limpia y renovable.</li>
            <li>Reducción en el consumo de energía convencional.</li>
            <li>Monitoreo en tiempo real.</li>
            <li>Bajo costo operativo a largo plazo.</li>
            <li>Promueve la conciencia ambiental.</li>
          </ul>
        </div>
        <div class="disadvantages">
          <h3>Desventajas</h3>
          <ul>
            <li>Depende de condiciones de viento favorables.</li>
            <li>Instalación inicial costosa.</li>
            <li>Mantenimiento periódico requerido.</li>
            <li>Eficiencia variable según ubicación.</li>
          </ul>
        </div>
      </div>
    </section>
    <!-- EQUIPO -->
    <section id="equipo">
      <h2>Equipo - Integrantes y Funciones</h2>
      <div class="team">
        <div class="member">
          <img src="https://th.bing.com/th/id/OIP.aHjynypJog2svK2GUN36iwHaFx?w=200&h=180&c=7&r=0&o=5&pid=1.7" alt="Foto de Rossiel">
          <h4>Rossiel</h4>
          <p>Coordinación general y supervisión del proyecto.</p>
        </div>
        <div class="member">
          <img src="data:image/jpeg;base64,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" alt="Foto de Maria">
          <h4>Maria</h4>
          <p>Diseño del sistema eólico y análisis de datos.</p>
        </div>
        <div class="member">
          <img src="https://th.bing.com/th/id/OIP.wXmV6zsmK1SSsvbLYxAcwQHaHa?w=195&h=194&c=7&r=0&o=5&pid=1.7" alt="Foto de Marisol">
          <h4>Marisol</h4>
          <p>Programación en Arduino y control de sensores.</p>
        </div>
        <div class="member">
          <img src="https://th.bing.com/th/id/OIP.LFdCdVVCxArUQIHHqddHvAHaHa?w=176&h=180&c=7&r=0&o=5&pid=1.7" alt="Foto de Samuel">
          <h4>Samuel</h4>
          <p>Integración del sistema eléctrico y pruebas de campo.</p>
        </div>
        <div class="member">
          <img src="data:image/jpeg;base64,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" alt="Foto de Johanser">
          <h4>Johanser</h4>
          <p>Optimización del consumo energético y modelado.</p>
        </div>
        <div class="member">
          <img src="https://th.bing.com/th/id/OIP.BX08iKGYaJmg44RvoN2TSAHaHa?w=182&h=182&c=7&r=0&o=5&pid=1.7" alt="Foto de Andonis">
          <h4>Adonis</h4>
          <p>Documentación y presentación de resultados.</p>
        </div>
        <div class="member">
            <img src="https://th.bing.com/th/id/OIP.nRaecf633vPkodgbuufMwAAAAA?w=115&h=180&c=7&r=0&o=5&pid=1.7" alt="Foto de angel">
            <h4>angel</h4>
            <p>CREADOR DE ESTILOS Y AFICHET</p>
      </div>
    
    </section>
    <!-- APLICACIÓN -->
    <section id="aplicacion">
      <h2>Aplicación en el Politécnico</h2>
      <p>
        El proyecto se integra en los planes de sostenibilidad del Politécnico, promoviendo la innovación y el compromiso ambiental. La instalación de prototipos de Windlight en áreas comunes sirve como ejemplo de eficiencia energética y fomenta la participación estudiantil en la investigación de energías renovables.
      </p>
      <p>
        Además, se exhibirá en ferias de ciencia y tecnología para demostrar su funcionamiento y generar datos para futuros estudios.
      </p>
    </section>
    <!-- CONCLUSIONES -->
    <section id="conclusion">
      <h2>Conclusiones</h2>
      <p>
        La implementación de <strong>Windlight</strong> muestra que la energía eólica puede ser aprovechada eficazmente para iluminación, siempre y cuando se cuente con un sistema de control adecuado. El uso de Arduino y sensores permite optimizar el consumo y evaluar la viabilidad del proyecto en diferentes entornos.
      </p>
      <p>
        Este tipo de soluciones no solo reduce costos energéticos, sino que también promueve una mayor conciencia ambiental. Se deben considerar factores como la velocidad del viento y el mantenimiento para asegurar su rendimiento óptimo.
      </p>
    </section>
    <!-- ANEXOS -->
    <section id="anexos">
      <h2>Anexos</h2>
      <p>A continuación, se muestran imágenes del proyecto, del equipo en acción y de prototipos:</p>
      <div class="gallery">
        <img src="https://th.bing.com/th/id/R.901894beb933f38c6aa2b7886fc64cec?rik=yCwDqMI4j0jgjA&pid=ImgRaw&r=0" alt="Prototipo 1">
        <img src="https://www.greenteach.es/wp-content/uploads/2018/11/energia-eolica-9.jpg" alt="Prototipo 2">
        <img src="https://th.bing.com/th/id/OIP.J5H9z49dwiGhZVFuRlsXFgHaHo?rs=1&pid=ImgDetMain" alt="Equipo trabajando">
      </div>
    </section>
  </div>
  <!-- PIE DE PÁGINA -->
  <footer>
    <p>© 2025 WINDLIGHT. Todos los derechos reservados.</p>
  </footer>
