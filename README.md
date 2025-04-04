<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
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
      background: url("data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAsJCQcJCQcJCQkJCwkJCQkJCQsJCwsMCwsLDA0QDBEODQ4MEhkSJRodJR0ZHxwpKRYlNzU2GioyPi0pMBk7IRP/2wBDAQcICAsJCxULCxUsHRkdLCwsLCwsLCwsLCwsLCwsLCwsLCwsLCwsLCwsLCwsLCwsLCwsLCwsLCwsLCwsLCwsLCz/wAARCAC0AN4DASIAAhEBAxEB/8") no-repeat center center;
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
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
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
       EQUIPO
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
  <main class="container">
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
          <img src="https://th.bing.com/th/id/OIP.nRaecf633vPkodgbuufMwAAAAA?w=115&h=180&c=7&r=0&o=5&pid=1.7" alt="Foto de Angel">
          <h4>Angel</h4>
          <p>Creador de estilos y afiche.</p>
        </div>
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
  </main>
  <!-- PIE DE PÁGINA -->
  <footer>
    <p>© 2025 WINDLIGHT. Todos los derechos reservados.</p>
  </footer>
</body>
</html>
