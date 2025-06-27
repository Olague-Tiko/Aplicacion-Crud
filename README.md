# Aplicacion-Crud
Segundo Proyecto de bootcam

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Landing Page - Mi Producto</title>
  <!-- Bootstrap CSS -->
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
  <!-- Estilos personalizados -->
  <style>
    /* Importar Google Fonts */
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');
   
    /* Estilos generales */
    body {
      font-family: 'Roboto', sans-serif;
      background-color: #f8f9fa;
      margin: 0;
      padding: 0;
    }
   
    /* =========================
       Navbar
    ============================ */
    .navbar {
      box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1);
    }
    .navbar-brand {
      font-weight: bold;
    }
   
    /* =========================
       Hero Section
    ============================ */
    .hero {
      background: url('https://naukas.com/fx/uploads/2013/02/img1-640x350.jpg') no-repeat center center;
      background-size: cover;
      color: white;
      position: relative;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
    }
    /* Overlay para mejorar la legibilidad */
    .hero::after {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.6);
    }
    .hero-content {
      position: relative;
      z-index: 2;
    }
    .hero h1 {
      font-size: 4rem;
      font-weight: bold;
    }
   
    /* =========================
       About Section
    ============================ */
    .about {
      padding: 80px 0;
    }
    .about-img {
      max-width: 100%;
      border-radius: 8px;
    }
   
    /* =========================
       Gallery Section
       Uso de CSS Grid para imágenes simétricas
    ============================ */
    .gallery {
      padding: 80px 0;
      background-color: #fff;
    }
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      grid-gap: 20px;
    }
    /* Cada contenedor mantiene un aspect ratio fijo (4:3) */
    .gallery-item {
      position: relative;
      width: 100%;
      height: 0;
      padding-bottom: 75%; /* Aspect ratio 4:3 */
      overflow: hidden;
      border-radius: 8px;
    }
    .gallery-item img {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover; /* Recorta la imagen para llenar el contenedor */
    }
   
    /* =========================
       Testimonials Section
    ============================ */
    .testimonials {
      padding: 80px 0;
      background-color: #f1f1f1;
    }
    .testimonial {
      background: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
      margin-bottom: 30px;
    }
   
    /* =========================
       Contact Section
    ============================ */
    #contact {
      background-color: #fff;
      padding: 80px 0;
    }
   
    /* =========================
       Footer
    ============================ */
    footer {
      background-color: #343a40;
      color: #ccc;
      padding: 20px 0;
    }
  </style>
</head>
<body>
  <!-- =========================
       Navbar
  ============================ -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container">
      <a class="navbar-brand" href="#">MiProducto</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav"
              aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item"><a class="nav-link" href="#hero">Inicio</a></li>
          <li class="nav-item"><a class="nav-link" href="#about">Acerca de</a></li>
          <li class="nav-item"><a class="nav-link" href="#gallery">Galería</a></li>
          <li class="nav-item"><a class="nav-link" href="#testimonials">Testimonios</a></li>
          <li class="nav-item"><a class="nav-link" href="#contact">Contacto</a></li>
        </ul>
      </div>
    </div>
  </nav>
 
  <!-- =========================
       Hero Section
  ============================ -->
  <section id="hero" class="hero">
  <div class="hero-content text-center">
    <h1>El Michi Cyberpunk</h1>
    
    <p class="lead" style="margin-top: 2cm;">Sala de lectura.</p>
    
    <a href="#about" class="btn btn-primary btn-lg" style="margin-top: 2cm; display: inline-block;">
      Conocer Actividades
    </a>
  </div>
  </section>
 
  <!-- =========================
       About Section
  ============================ -->
  <section id="about" class="about">
    <div class="container">
      <div class="row align-items-center">
        <!-- Texto descriptivo -->
        <div class="col-md-6">
          <h2>Acerca de Nosotros</h2>
          <p>Somos una sala de lectura en línea que disfruta de compartir esta actividad de diferentes maneras.</p>
          <p>No se necesita tener la lectura en libros físicos. Nos encanta compartir la lectura digital ya que consideramos que es más accesible a través de un teléfono celular.</p>
          <p>Te invitamos a compartir esta actividad sin que te sientas obligado a leer. El objetivo principal es compartir ideas en torno a un texto.</p>
          <p>Principalmente disfrutamos de contenido de ciencia ficción. Pero la sala está hecha para todos los gustos, todas las edades y todos los géneros literarios.</p>
        </div>
        <!-- Imagen descriptiva -->
        <div class="col-md-6">
          <img src="https://static.vecteezy.com/system/resources/previews/030/652/304/large_2x/cyberpunk-cat-neon-free-photo.jpg" alt="Acerca de nosotros" class="about-img" style="margin-left: 2cm">
        </div>
      </div>
    </div>
  </section>
 
  <!-- =========================
       Gallery Section
       Sección de Galería con 8 productos
  ============================ -->
  <section id="gallery" class="gallery">
    <div class="container">
      <h2 class="text-center mb-5">Galería</h2>
      <div class="gallery-grid">
        <!-- Producto 1 -->
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Producto 1">
        </div>
        <!-- Producto 2 -->
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1564869739735-722eb8c5b310?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Producto 2">
        </div>
        <!-- Producto 3 -->
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1611078484821-1abf8cbd64e1?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Producto 3">
        </div>
        <!-- Producto 4 -->
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1581291519195-ef11498d1cf2?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Producto 4">
        </div>
        <!-- Producto 5 -->
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1556740749-887f6717d7e4?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Producto 5">
        </div>
        <!-- Producto 6 -->
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1595433324234-cf80d466dd3c?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Producto 6">
        </div>
        <!-- Producto 7 -->
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1572432038751-05d2d189e8e2?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Producto 7">
        </div>
        <!-- Producto 8 -->
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1572432038754-1e581c04dd1a?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Producto 8">
        </div>
      </div>
    </div>
  </section>
 
  <!-- =========================
       Testimonials Section
  ============================ -->
  <section id="testimonials" class="testimonials">
    <div class="container">
      <h2 class="text-center mb-5">Testimonios</h2>
      <div class="row">
        <div class="col-md-4">
          <div class="testimonial">
            <p>"MiProducto ha cambiado mi forma de trabajar. ¡Es increíble!"</p>
            <h5 class="mt-3">Juan Pérez</h5>
          </div>
        </div>
        <div class="col-md-4">
          <div class="testimonial">
            <p>"La innovación y calidad de este producto son insuperables."</p>
            <h5 class="mt-3">María López</h5>
          </div>
        </div>
        <div class="col-md-4">
          <div class="testimonial">
            <p>"Recomiendo MiProducto a todos los que buscan eficiencia y estilo."</p>
            <h5 class="mt-3">Carlos Sánchez</h5>
          </div>
        </div>
      </div>
    </div>
  </section>
 
  <!-- =========================
       Contact Section
  ============================ -->
  <section id="contact" class="py-5">
    <div class="container">
      <h2 class="text-center mb-5">Contacto</h2>
      <div class="row">
        <div class="col-md-8 offset-md-2">
          <form>
            <!-- Campo de nombre -->
            <div class="form-group">
              <label for="name">Nombre</label>
              <input type="text" class="form-control" id="name" placeholder="Ingresa tu nombre">
            </div>
            <!-- Campo de correo -->
            <div class="form-group">
              <label for="email">Correo electrónico</label>
              <input type="email" class="form-control" id="email" placeholder="Ingresa tu correo">
            </div>
            <!-- Campo de mensaje -->
            <div class="form-group">
              <label for="message">Mensaje</label>
              <textarea class="form-control" id="message" rows="5" placeholder="Escribe tu mensaje"></textarea>
            </div>
            <!-- Botón de enviar -->
            <button type="submit" class="btn btn-primary btn-block">Enviar</button>
          </form>
        </div>
      </div>
    </div>
  </section>
 
  <!-- =========================
       Footer
  ============================ -->
  <footer class="text-center">
    <div class="container">
      <p>&copy; 2025 MiProducto, Inc. Todos los derechos reservados.</p>
    </div>
  </footer>
 
  <!-- Scripts de Bootstrap y jQuery -->
  <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
