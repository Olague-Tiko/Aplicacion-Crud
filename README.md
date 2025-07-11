<!DOCTYPE html>
<html lang="es">
<head>

<meta charset="UTF-8">
  <title>CRUD Literario</title>
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
  <style>
    .form-section { margin-bottom: 30px; }
    .table td, .table th { vertical-align: middle; }
  </style>

  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Landing Page - Sala de lectura</title>
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

  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Testimonios</title>

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" />

  <!-- Estilos personalizados para los controles del carrusel -->
  <style>
    /* Quitamos los iconos originales */
    .carousel-control-prev-icon,
    .carousel-control-next-icon {
      display: none;
    }

    /* Botones con forma OVNI (ovalo ancho) */
    .carousel-control-prev,
    .carousel-control-next {
      background-color: rgba(0, 0, 0, 0.7);
      border-radius: 50px;
      width: 130px;
      height: 45px;
      display: flex;
      align-items: center;
      justify-content: center;
      top: 50%;
      transform: translateY(-50%);
      opacity: 0.85;
      transition: background-color 0.3s ease, opacity 0.3s ease;
      color: white;
      font-weight: 600;
      font-size: 1rem;
      text-transform: uppercase;
      border: 2px solid transparent;
      user-select: none;
      cursor: pointer;
    }

    .carousel-control-prev:hover,
    .carousel-control-next:hover {
      background-color: rgba(0, 0, 0, 0.9);
      opacity: 1;
      border-color: white;
    }

    /* Posicionar los botones un poco más adentro */
    .carousel-control-prev {
      left: 15px;
    }
    .carousel-control-next {
      right: 15px;
    }
   
    /* =========================
       Contact Section
    ============================ */
    meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1" />
      <title>Registro Lector CRUD con Historial</title>
      <link href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.0/dist/css/bootstrap.min.css" rel="stylesheet" />
    
    
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

<!-- Bootstrap Bundle JS (incluye Popper) -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

<body>
  <!-- =========================
       Navbar
  ============================ -->
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container">
    <a class="navbar-brand" href="#">El michi cyberpunk</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav"
            aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ml-auto">
        <li class="nav-item"><a class="nav-link" href="#hero">Inicio</a></li>
        <li class="nav-item"><a class="nav-link" href="#about">Acerca de</a></li>
        <li class="nav-item"><a class="nav-link" href="#gallery">Galería</a></li>
        <li class="nav-item"><a class="nav-link" href="#testimonials">Comentarios</a></li>
        <li class="nav-item"><a class="nav-link" href="#contact">Contacto</a></li>
      </ul>
    </div>
  </div>
</nav>

<style>
  /* Estilo al pasar el mouse por un enlace del menú */
  .navbar-nav .nav-link:hover {
    background-color: #000;        /* Fondo negro */
    color: #fff !important;        /* Texto blanco */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.4);
    border-radius: 6px;
    padding: 6px 12px;
    transition: all 0.3s ease;
  }
</style>
 
  <!-- =========================
       Hero Section
  ============================ -->
  <section id="hero" class="hero">
  <div class="hero-content text-center">
    <h1>El Michi Cyberpunk</h1>
    
    <p class="lead" style="margin-top: 2cm;">Sala de lectura.</p>
    
    <a href="#about" class="btn btn-primary btn-lg" style="margin-top: 2cm; display: inline-block;">
      Conocer más
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
    <div class="gallery-grid d-flex flex-wrap justify-content-center gap-3">
      <!-- Producto 1 -->
      <div class="gallery-item">
        <img src="https://covers.storytel.com/jpg-640/9788445004760.8baca47a-b2f8-4a49-818b-969e173714d2?optimize=high&quality=70&width=600" alt="Producto 1" class="img-clickable">
      </div>
      <!-- Producto 2 -->
      <div class="gallery-item">
        <img src="https://imagessl0.casadellibro.com/a/l/s5/40/9788435021340.webp" alt="Producto 2" class="img-clickable">
      </div>
      <!-- Producto 3 -->
      <div class="gallery-item">
        <img src="https://www.elsotano.com/sotano_covers/9788418/9788418765148.jpg" alt="Producto 3" class="img-clickable">
      </div>
      <!-- Producto 4 -->
      <div class="gallery-item">
        <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiR7Ww5sx1TO6poz2N3Jy0m0khozarqXwp64VxnYF-0RK35kZL2tSnWlDRxVidbiiIwuQsFH10_uMCGaQHLzqmG01lg78XHTjFboGdL2C7Pek9JTRbRTCw4ySDrS8eCDjZ3FtOQAgcwwV-7/s320/Dune%252C+de+Frank+Herbert.jpg" alt="Producto 4" class="img-clickable">
      </div>
    </div>
  </div>
</section>

<!-- Modal de imagen -->
<div class="modal fade" id="imageModal" tabindex="-1" aria-labelledby="imageModalLabel" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered modal-xl">
    <div class="modal-content bg-dark">
      <div class="modal-body p-0 d-flex justify-content-center align-items-center" style="height: 100vh;">
        <img src="" alt="Vista previa" id="modalImage" class="img-fluid modal-img" />
      </div>
    </div>
  </div>
</div>

<style>
  .gallery-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }

  .gallery-item {
    width: 200px;
    height: 300px;
    overflow: hidden;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
    cursor: pointer;
  }

  .gallery-item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.3s ease;
  }

  .gallery-item img:hover {
    transform: scale(1.05);
  }

  .modal-img {
    max-height: 90vh;         /* Imagen no supera el 90% de la pantalla */
    max-width: 95vw;          /* Ancho máximo del viewport */
    object-fit: contain;      /* Asegura que se vea toda sin recorte */
    border-radius: 10px;
  }

  .modal-content {
    background-color: transparent;
    border: none;
    box-shadow: none;
  }
</style>

<!-- JavaScript para mostrar la imagen en el modal -->
<script>
  document.querySelectorAll('.img-clickable').forEach(img => {
    img.addEventListener('click', function () {
      const modalImg = document.getElementById('modalImage');
      modalImg.src = this.src;
      const imageModal = new bootstrap.Modal(document.getElementById('imageModal'));
      imageModal.show();
    });
  });
</script>

<!-- Bootstrap JS (asegúrate de incluir esto si no lo tienes ya) -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
 
  <!-- =========================
       Testimonials Section
  ============================ -->
 <section id="testimonials" class="testimonials">
    <div class="container">
      <h2 class="text-center mb-5">Comentarios</h2>

      <div id="testimonialCarousel" class="carousel slide carousel-fade" data-bs-ride="carousel" data-bs-interval="8000">
        <div class="carousel-inner text-center">

          <div class="carousel-item active">
            <div class="testimonial mx-auto" style="max-width: 700px;">
              <p>"Me encanta el círculo de lectura por la noche. Disfruto compartir ideas y me sirve para relajarme entre semana sin salir de casa".</p>
              <h5 class="mt-3">Andres Manuel López Obrador</h5>
            </div>
          </div>

          <div class="carousel-item">
            <div class="testimonial mx-auto" style="max-width: 700px;">
              <p>"Alberto es un buen moderador. Fomenta la participación y también nos invita a que nosotros propongamos lecturas para las sesiones".</p>
              <h5 class="mt-3">Cucho</h5>
            </div>
          </div>

          <div class="carousel-item">
            <div class="testimonial mx-auto" style="max-width: 700px;">
              <p>"Les recomiendo participar en las actividades. Me gusta que no siento como si debiera leer por obligación como en la escuela y disfruto más la lectura".</p>
              <h5 class="mt-3">Kevin Mier</h5>
            </div>
          </div>

          <div class="carousel-item">
            <div class="testimonial mx-auto" style="max-width: 700px;">
              <p>"Me fascina la ciencia ficción y creo que encontré el lugar correcto para explorar, literalmente, nuevos mundos".</p>
              <h5 class="mt-3">Melisandre Olague</h5>
            </div>
          </div>

          <div class="carousel-item">
            <div class="testimonial mx-auto" style="max-width: 700px;">
              <p>"No sabía cuánto existía referente a la ciencia ficción. Lo mejor es que no solo leemos, sino también vemos películas y las comentamos".</p>
              <h5 class="mt-3">Kariniwi</h5>
            </div>
          </div>

        </div>

        <!-- Controles -->
        <button class="carousel-control-prev" type="button" data-bs-target="#testimonialCarousel" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Anterior</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#testimonialCarousel" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Siguiente</span>
        </button>
      </div>
    </div>
  </section>

  <!-- Bootstrap JS Bundle (incluye Popper) -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

 
  <!-- =========================
       Contact Section
  ============================ -->
<!-- Formulario de contacto -->
<!-- Contenedor único para mostrar el registro del usuario -->
<div class="container py-5">
  <h2 class="text-center mb-4">Registro Lector</h2>

  <div id="usuarioRegistroPanel">
    <!-- Aquí se cargará el registro del usuario -->
  </div>

  <!-- Formulario -->
  <div class="form-section">
    <form id="crudForm">
      <input type="hidden" id="registroId" value="">
      <div class="form-group">
        <label>Nombre</label>
        <input type="text" id="name" class="form-control" required>
      </div>
      <div class="form-group">
        <label>Correo electrónico</label>
        <input type="email" id="email" class="form-control" required>
      </div>
      <div class="form-group">
        <label>¿Por qué quieres participar?</label>
        <textarea id="message" class="form-control" rows="3" required></textarea>
      </div>
      <div class="form-group">
        <label>Género literario favorito</label>
        <select id="genero" class="form-control" required>
          <option value="" disabled selected>Selecciona un género</option>
          <option value="fantasia">Fantasía</option>
          <option value="ciencia-ficcion">Ciencia Ficción</option>
          <option value="romance">Romance</option>
          <option value="misterio">Misterio</option>
          <option value="no-ficcion">No ficción</option>
          <option value="otro">Otro</option>
        </select>
      </div>
      <div class="form-group">
        <label>Actividades</label><br>
        <div class="form-check">
          <input class="form-check-input actividad" type="checkbox" value="circulo" id="circulo">
          <label class="form-check-label" for="circulo">Círculo de lectura</label>
        </div>
        <div class="form-check">
          <input class="form-check-input actividad" type="checkbox" value="blog" id="blog">
          <label class="form-check-label" for="blog">Reseñas en blog</label>
        </div>
        <div class="form-check">
          <input class="form-check-input actividad" type="checkbox" value="video" id="video">
          <label class="form-check-label" for="video">Video-reseñas</label>
        </div>
      </div>
      <button type="submit" class="btn btn-primary btn-block">Guardar</button>
    </form>
  </div>
</div>

<script>
  let registros = JSON.parse(localStorage.getItem("registrosLiterarios")) || [];
  let historial = JSON.parse(localStorage.getItem("historialCambios")) || [];
  let registroActual = localStorage.getItem("registroActual");

  // Renderiza solo el registro del usuario actual o mensaje si no existe
  function renderUsuarioRegistro() {
    const panel = document.getElementById("usuarioRegistroPanel");
    panel.innerHTML = "";

    if (registroActual === null || !registros[registroActual]) {
      panel.innerHTML = `<p>No tienes un registro todavía. Por favor llena el formulario para crear uno.</p>`;
      return;
    }

    const r = registros[registroActual];
    const finalizado = r.finalizado ? true : false;

    let actividadesText = r.actividades.join(", ");

    let acciones = "";

    if (!finalizado) {
      acciones = `
        <button class="btn btn-warning mr-2" onclick="editarRegistro(${registroActual})">Editar mi registro</button>
        <button class="btn btn-danger mr-2" onclick="eliminarRegistro(${registroActual})">Eliminar mi registro</button>
        <button class="btn btn-success" onclick="finalizarRegistro(${registroActual})">Finalizar mi registro</button>
      `;
    } else {
      acciones = `<span class="text-success font-weight-bold">Registro finalizado</span>`;
    }

    panel.innerHTML = `
      <table class="table table-bordered w-75 mx-auto">
        <tr><th>Nombre</th><td>${r.name}</td></tr>
        <tr><th>Correo</th><td>${r.email}</td></tr>
        <tr><th>Mensaje</th><td>${r.message}</td></tr>
        <tr><th>Género literario favorito</th><td>${r.genero}</td></tr>
        <tr><th>Actividades</th><td>${actividadesText}</td></tr>
        <tr><th>Acciones</th><td>${acciones}</td></tr>
      </table>
    `;
  }

  function guardarEnLocalStorage() {
    localStorage.setItem("registrosLiterarios", JSON.stringify(registros));
    localStorage.setItem("historialCambios", JSON.stringify(historial));
  }

  function registrarCambio(id, campo, anterior, nuevo) {
    historial.push({
      idRegistro: id,
      campo,
      anterior,
      nuevo,
      fecha: new Date().toLocaleString()
    });
    guardarEnLocalStorage();
  }

  function registrarEliminacion(idRegistro, datosEliminados) {
  const historial = JSON.parse(localStorage.getItem("historialCambios")) || [];

  historial.push({
    idRegistro: idRegistro,
    accion: "eliminacion",
    datos: datosEliminados,
    fecha: new Date().toLocaleString()
  });

  localStorage.setItem("historialCambios", JSON.stringify(historial));
}

  document.getElementById("crudForm").addEventListener("submit", function (e) {
    e.preventDefault();

    const id = document.getElementById("registroId").value;
    const name = document.getElementById("name").value.trim();
    const email = document.getElementById("email").value.trim().toLowerCase();
    const message = document.getElementById("message").value.trim();
    const genero = document.getElementById("genero").value;
    const actividades = Array.from(document.querySelectorAll(".actividad:checked")).map(el => el.value);

    if (!name || !email || !message || !genero || actividades.length === 0) {
      alert("Faltan campos por llenar.");
      return;
    }

    const nuevoRegistro = { name, email, message, genero, actividades, finalizado: false };

    if (id === "") {
      // Crear nuevo registro
      registros.push(nuevoRegistro);
      registroActual = (registros.length - 1).toString();
      localStorage.setItem("registroActual", registroActual);
      registrarCambio(registroActual, "CREAR", "", JSON.stringify(nuevoRegistro));
    } else {
      const index = parseInt(id);
      const original = registros[index];
      if (original.finalizado) {
        alert("Este registro está finalizado y no puede modificarse.");
        return;
      }

      if (original.name !== name) registrarCambio(index, "name", original.name, name);
      if (original.email !== email) registrarCambio(index, "email", original.email, email);
      if (original.message !== message) registrarCambio(index, "message", original.message, message);
      if (original.genero !== genero) registrarCambio(index, "genero", original.genero, genero);

      const originalActividades = original.actividades.sort().join(",");
      const nuevasActividades = actividades.sort().join(",");
      if (originalActividades !== nuevasActividades) {
        registrarCambio(index, "actividades", originalActividades, nuevasActividades);
      }

      nuevoRegistro.finalizado = original.finalizado;
      registros[index] = nuevoRegistro;
    }

    guardarEnLocalStorage();
    renderUsuarioRegistro();
    this.reset();
    document.getElementById("registroId").value = "";
  });

  function editarRegistro(index) {
    const r = registros[index];
    if (r.finalizado) {
      alert("Este registro está finalizado y no puede modificarse.");
      return;
    }
    document.getElementById("registroId").value = index;
    document.getElementById("name").value = r.name;
    document.getElementById("email").value = r.email;
    document.getElementById("message").value = r.message;
    document.getElementById("genero").value = r.genero;

    document.querySelectorAll(".actividad").forEach(cb => {
      cb.checked = r.actividades.includes(cb.value);
    });
  }

  function eliminarRegistro(index) {
  if (confirm("¿Estás seguro de eliminar este registro?")) {
    registrarEliminacion(index, registros[index]); // Guarda el historial antes de eliminar
    registros.splice(index, 1);
    localStorage.setItem("registrosLiterarios", JSON.stringify(registros));
    renderizarTabla();
  }
}

  function finalizarRegistro(index) {
    if (confirm("¿Deseas finalizar tu registro? No podrás modificarlo después.")) {
      registros[index].finalizado = true;
      registrarCambio(index, "FINALIZAR", "", "Registro finalizado");
      guardarEnLocalStorage();
      renderUsuarioRegistro();
      document.getElementById("crudForm").reset();
      document.getElementById("registroId").value = "";
    }
  }

  // Inicializar vista
  renderUsuarioRegistro();
</script>

  <!-- =========================
       Footer
  ============================ -->
  <footer class="text-center">
    <div class="container">
      <p>&copy; 2025 Tikosolutions, Inc. Todos los derechos reservados.</p>
    </div>
  </footer>
 
  <!-- Scripts de Bootstrap y jQuery -->
  <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
