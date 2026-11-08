# mi-clase-de-computacion
<!-- Indica la versión de HTML que se está utilizando para el navegador -->
<!DOCTYPE html>
<!-- Define el idioma principal del documento como español -->
<html lang="es">
<!-- Inicio del encabezado del documento que contiene metadatos y estilos -->
<head>
  <!-- Define la codificación de caracteres para soportar tildes y caracteres especiales -->
  <meta charset="UTF-8">
  <!-- Define la configuración de la pantalla para ser adaptable a dispositivos móviles -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Define el título de la pestaña del navegador -->
  <title>Buscador Interactivo y Galería Multimedia</title>
  <!-- Inicio del bloque de estilos CSS -->
  <style>
    /* Selecciona todos los elementos para reiniciar márgenes y rellenos por defecto */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    /* Configura el fondo general en tono cálido y la tipografía a Georgia */
    body { font-family: 'Georgia', serif; background-color: #fef9c3; color: #1e1b4b; line-height: 1.6; }
    /* Estila el encabezado principal del buscador con fondo verde suave */
    .buscador-header { background-color: #15803d; color: #ffffff; padding: 3rem 1.5rem; text-align: center; border-bottom: 5px solid #ca8a04; }
    /* Modifica el tamaño y espaciado del título principal */
    .buscador-header h1 { margin-bottom: 1.5rem; font-size: 2.5rem; text-transform: uppercase; letter-spacing: 2px; }
    /* Alinea el formulario de búsqueda usando flexbox centrado */
    .form-busqueda { display: flex; justify-content: center; gap: 1rem; flex-wrap: wrap; }
    /* Aplica estilos al campo de entrada de texto */
    .form-busqueda input { width: 70%; max-width: 450px; padding: 1rem 1.2rem; border: 3px solid #facc15; border-radius: 25px; font-size: 1.1rem; outline: none; background-color: #ffffff; }
    /* Cambia el aspecto del botón de búsqueda a un tono anaranjado */
    .form-busqueda button { background-color: #ea580c; color: #ffffff; border: 2px solid #9a3412; padding: 1rem 2rem; border-radius: 25px; cursor: pointer; font-weight: 800; font-size: 1rem; transition: all 0.3s ease; }
    /* Agrega un efecto interactivo al pasar el cursor sobre el botón */
    .form-busqueda button:hover { background-color: #c2410c; transform: scale(1.05); }
    /* Contenedor principal de los resultados de búsqueda */
    .resultados { max-width: 900px; margin: 3rem auto; padding: 0 1.5rem; }
    /* Estila el mensaje de resumen de resultados */
    .resumen { color: #854d0e; margin-bottom: 2rem; font-style: italic; font-size: 1.1rem; font-weight: 600; }
    /* Tarjeta individual de cada resultado con sombra y fondo blanco */
    .resultado { border: 2px solid #fde047; border-radius: 12px; padding: 1.5rem; margin-bottom: 1.5rem; background-color: #ffffff; box-shadow: 0 4px 6px rgba(0,0,0,0.05); }
    /* Tamaño y margen del título de cada resultado */
    .resultado h2 { font-size: 1.4rem; margin-bottom: 0.5rem; }
    /* Estilo del enlace dentro del resultado */
    .resultado a { color: #b45309; text-decoration: none; font-weight: bold; }
    /* Efecto al pasar el puntero sobre los enlaces */
    .resultado a:hover { color: #78350f; text-decoration: underline; }
    /* Texto descriptivo dentro del resultado */
    .resultado p { color: #374151; font-size: 1rem; margin-bottom: 1rem; }
    /* Contenedor de las miniaturas de imágenes */
    .thumb-container { display: flex; gap: 1rem; margin-top: 1rem; }
    /* Estilo de las imágenes pequeñas explicativas */
    .thumb-img { width: 120px; height: 90px; object-fit: cover; border-radius: 8px; border: 2px solid #ca8a04; }
    /* Sección adicional para alojar multimedia como audio y video */
    .seccion-multimedia { background-color: #fef08a; border: 2px dashed #ca8a04; padding: 2rem; border-radius: 15px; margin-top: 2rem; text-align: center; }
    /* Título secundario dentro de la sección multimedia */
    .seccion-multimedia h3 { margin-bottom: 1rem; color: #713f12; }
    /* Estila el elemento de reproducción de video */
    .video-demo { width: 100%; max-width: 500px; border-radius: 10px; border: 3px solid #15803d; margin-top: 1rem; }
    /* Estila el reproductor de audio */
    .audio-demo { margin-top: 1rem; width: 80%; }
    /* Pie de página con información de derechos y diseño */
    .sitio-footer { text-align: center; padding: 2rem; background-color: #713f12; color: #fef9c3; margin-top: 3rem; }
  /* Fin del bloque de estilos CSS */
  </style>
<!-- Fin del encabezado del documento -->
</head>
<!-- Inicio del cuerpo interactivo de la página -->
<body>
  <!-- Encabezado superior que contiene el motor de búsqueda -->
  <header class="buscador-header">
    <!-- Título principal de la sección de búsqueda -->
    <h1>Buscador de Productos</h1>
    <!-- Formulario para realizar búsquedas dentro del sitio -->
    <form class="form-busqueda" action="#" method="get">
      <!-- Campo para introducir el texto a buscar -->
      <input type="text" name="q" placeholder="Buscar tenis, botas o accesorios..." value="zapatos">
      <!-- Botón para enviar la búsqueda -->
      <button type="submit">Buscar</button>
    <!-- Fin del formulario -->
    </form>
  <!-- Fin del encabezado principal -->
  </header>

  <!-- Sección de contenido principal que despliega los resultados -->
  <main class="resultados">
    <!-- Texto que indica la cantidad de resultados devueltos -->
    <p class="resumen">Se encontraron 3 resultados para "zapatos"</p>

    <!-- Primer artículo de resultado de búsqueda -->
    <article class="resultado">
      <!-- Encabezado con enlace al primer producto -->
      <h2><a href="#">Recurso Visual 1: Zapatos Deportivos Running</a></h2>
      <!-- Descripción corta del primer producto -->
      <p>Diseño aerodinámico con suela amortiguada para alto rendimiento deportivo.</p>
      <!-- Contenedor para imágenes de muestra -->
      <div class="thumb-container">
        <!-- Recurso Visual 1: Imagen del primer producto -->
        <img class="thumb-img" src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=300" alt="Zapatos Deportivos">
        <!-- Recurso Visual 2: Segunda imagen del primer producto -->
        <img class="thumb-img" src="https://images.unsplash.com/photo-1608231387042-66d1773070a5?w=300" alt="Zapatos vista lateral">
      <!-- Fin del contenedor de miniaturas -->
      </div>
    <!-- Fin del primer resultado -->
    </article>

    <!-- Segundo artículo de resultado de búsqueda -->
    <article class="resultado">
      <!-- Encabezado con enlace al segundo producto -->
      <h2><a href="#">Recurso Visual 2: Zapatos Casuales Urbanos</a></h2>
      <!-- Descripción corta del segundo producto -->
      <p>Comodidad para el día a día elaborados con materiales de alta durabilidad.</p>
      <!-- Contenedor para imágenes de muestra -->
      <div class="thumb-container">
        <!-- Recurso Visual 3: Imagen del segundo producto -->
        <img class="thumb-img" src="https://images.unsplash.com/photo-1525966222134-fcfa99b8ae77?w=300" alt="Zapatos Casuales">
      <!-- Fin del contenedor de miniaturas -->
      </div>
    <!-- Fin del segundo resultado -->
    </article>

    <!-- Tercer artículo de resultado de búsqueda -->
    <article class="resultado">
      <!-- Encabezado con enlace al tercer producto -->
      <h2><a href="#">Recurso Visual 3: Zapatos de Vestir Elegantes</a></h2>
      <!-- Descripción corta del tercer producto -->
      <p>Elegancia en cuero legítimo ideal para reuniones formales y eventos.</p>
    <!-- Fin del tercer resultado -->
    </article>

    <!-- Sección multimedia integrada al diseño -->
    <section class="seccion-multimedia">
      <!-- Título de la sección de demostración -->
      <h3>Demostración de Productos y Ambiente</h3>
      <!-- Recurso Visual 4: Video demostrativo -->
      <video class="video-demo" controls poster="https://images.unsplash.com/photo-1595950653106-6c9ebd614d3a?w=500">
        <!-- Fuente de video en formato MP4 -->
        <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
        <!-- Mensaje en caso de que el navegador no ejecute el video -->
        Tu navegador no soporta la reproducción de video.
      <!-- Fin del elemento de video -->
      </video>
      <br>
      <!-- Recurso Visual 5: Audio de ambiente -->
      <audio class="audio-demo" controls>
        <!-- Fuente de audio de muestra -->
        <source src="https://www.w3schools.com/html/horse.ogg" type="audio/ogg">
        <!-- Mensaje en caso de que el navegador no ejecute el audio -->
        Tu navegador no soporta el elemento de audio.
      <!-- Fin del elemento de audio -->
      </audio>
    <!-- Fin de la sección multimedia -->
    </section>
  <!-- Fin del contenedor principal -->
  </main>

  <!-- Pie de página con créditos de desarrollo -->
  <footer class="sitio-footer">
    <!-- Texto de derechos reservados -->
    <p>&copy; 2026 Buscador Interactivo - Todos los derechos reservados.</p>
  <!-- Fin del pie de página -->
  </footer>
<!-- Fin del cuerpo del documento -->
</body>
<!-- Fin del archivo HTML -->
</html>
