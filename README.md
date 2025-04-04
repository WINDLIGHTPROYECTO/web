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
      background: url("data:image/jpeg;base64,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") no-repeat center center;
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
    /* ============================
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
      transition: background 0.3s ease, transform 0.3s ease;
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
          <img src="https://sdmntpreastus2.oaiusercontent.com/files/00000000-b45c-51f6-97c6-e7e88571a1f9/raw?se=2025-04-04T02%3A02%3A15Z&sp=r&sv=2024-08-04&sr=b&scid=a12bc5a8-1204-5912-8059-a02075dbe2bd&skoid=ac1d63ad-0c69-4017-8785-7a50eb04382c&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-04-03T23%3A03%3A37Z&ske=2025-04-04T23%3A03%3A37Z&sks=b&skv=2024-08-04&sig=ksmO1nddzTcKl7xoLe8Vf1qBlY16wMso0%2BM5AZnpzNw%3D" alt="Foto de Rossiel">
          <h4>Rossiel</h4>
          <p>Coordinación general y supervisión del proyecto.</p>
        </div>
        <div class="member">
          <img src="https://sdmntpreastus2.oaiusercontent.com/files/00000000-98a4-51f6-9085-2823483aab96/raw?se=2025-04-04T01%3A59%3A34Z&sp=r&sv=2024-08-04&sr=b&scid=66e3435b-a849-5527-b883-6b5f9c38abd8&skoid=ac1d63ad-0c69-4017-8785-7a50eb04382c&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-04-03T16%3A09%3A13Z&ske=2025-04-04T16%3A09%3A13Z&sks=b&skv=2024-08-04&sig=Bnu2TyD5qo2Mf4FsWDoGAHT7%2BUa4UsdJYvNqT07zGl8%3D" alt="Foto de Maria">
          <h4>Maria</h4>
          <p>Diseño del sistema eólico y análisis de datos.</p>
        </div>
        <div class="member">
          <img src="https://th.bing.com/th/id/OIP.wXmV6zsmK1SSsvbLYxAcwQHaHa?w=195&h=194&c=7&r=0&o=5&pid=1.7" alt="Foto de Marisol">
          <h4>Marisol</h4>
          <p>Programación en Arduino y control de sensores.</p>
        </div>
        <div class="member">
          <img src="https://sdmntpreastus2.oaiusercontent.com/files/00000000-c38c-51f6-aa7a-3899e13b60dc/raw?se=2025-04-04T02%3A03%3A02Z&sp=r&sv=2024-08-04&sr=b&scid=f3e75395-51d9-57f2-b9ed-be92253b4139&skoid=ac1d63ad-0c69-4017-8785-7a50eb04382c&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-04-03T21%3A39%3A37Z&ske=2025-04-04T21%3A39%3A37Z&sks=b&skv=2024-08-04&sig=EEv4TSMkQL6fJ0LW0LLloZrQy5%2B5GhjbZhN/2h8GbUY%3D" alt="Foto de Samuel">
          <h4>Samuel</h4>
          <p>Integración del sistema eléctrico y pruebas de campo.</p>
        </div>
        <div class="member">
          <img src="https://sdmntpreastus2.oaiusercontent.com/files/00000000-ca00-51f6-83b9-e6e92afad2b4/raw?se=2025-04-04T01%3A58%3A53Z&sp=r&sv=2024-08-04&sr=b&scid=833c170a-b3ba-5c28-ba6f-1005b0234863&skoid=ac1d63ad-0c69-4017-8785-7a50eb04382c&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-04-03T16%3A12%3A16Z&ske=2025-04-04T16%3A12%3A16Z&sks=b&skv=2024-08-04&sig=13V4oLeO3u0uIx/XBq9G5oLGbLslpvMHAvS/eDtgJiQ%3D" alt="Foto de Johanser">
          <h4>Johanser</h4>
          <p>Optimización del consumo energético y modelado.</p>
        </div>
        <div class="member">
          <img src="https://sdmntpreastus2.oaiusercontent.com/files/00000000-b184-51f6-8762-91cb40b8f094/raw?se=2025-04-04T02%3A01%3A27Z&sp=r&sv=2024-08-04&sr=b&scid=040b6aca-a4c7-5477-a333-051a11ba7e11&skoid=ac1d63ad-0c69-4017-8785-7a50eb04382c&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-04-03T21%3A18%3A03Z&ske=2025-04-04T21%3A18%3A03Z&sks=b&skv=2024-08-04&sig=azhcj91msL3%2Bg%2ByGftx3pj6NU4fFjbZtGM01BpsWmwg%3D" alt="Foto de Andonis">
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
</body>
</html>
