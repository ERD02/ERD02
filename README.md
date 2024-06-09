- 👋 Hi, I’m @ERD02
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
ERD02/ERD02 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
---><!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Electroservice - Cursos de Electricidad y Refrigeración</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <header>
        <h1>Electroservice</h1>
        <nav>
            <a href="index.html">Inicio</a>
            <a href="cursos.html">Cursos</a>
            <a href="registro.html">Registro</a>
        </nav>
    </header>
    <main>
        <section>
            <h2>Bienvenido a Electroservice</h2>
            <p>Aprende a tu propio ritmo con nuestros cursos diseñados para darte las habilidades que necesitas en solo 3 meses.</p>
            <div class="botones">
                <a href="cursos.html?curso=electricidad" class="btn">Ver Curso de Electricidad</a>
                <a href="cursos.html?curso=refrigeracion" class="btn">Ver Curso de Refrigeración</a>
            </div>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Electroservice</p>
    </footer>
</body>
</html>

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cursos - Electroservice</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <header>
        <h1>Cursos</h1>
        <nav>
            <a href="index.html">Inicio</a>
            <a href="cursos.html">Cursos</a>
            <a href="registro.html">Registro</a>
        </nav>
    </header>
    <main>
        <section id="contenido-curso">
            <!-- El contenido del curso se llenará dinámicamente con JavaScript -->
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Electroservice</p>
    </footer>
    <script src="scripts.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registro - Electroservice</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <header>
        <h1>Registro</h1>
        <nav>
            <a href="index.html">Inicio</a>
            <a href="cursos.html">Cursos</a>
            <a href="registro.html">Registro</a>
        </nav>
    </header>
    <main>
        <section>
            <h2>Formulario de Registro</h2>
            <form action="https://formspree.io/f/{tu_email}" method="POST">
                <label for="nombre">Nombre Completo:</label>
                <input type="text" id="nombre" name="nombre" required>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="telefono">Número de Teléfono:</label>
                <input type="tel" id="telefono" name="telefono" required>

                <label for="curso">Selecciona el Curso:</label>
                <select id="curso" name="curso">
                    <option value="electricidad">Electricidad</option>
                    <option value="refrigeracion">Refrigeración</option>
                </select>

                <label for="cuenta">Número de Cuenta Bancaria para Depositar:</label>
                <input type="text" id="cuenta" name="cuenta" required>

                <input type="submit" value="Enviar">
            </form>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Electroservice</p>
    </footer>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header {
    background-color: #333;
    color: white;
    padding: 10px 20px;
    text-align: center;
}

nav a {
    color: white;
    margin: 0 10px;
    text-decoration: none;
}

main {
    padding: 20px;
}

section {
    margin: 20px 0;
}

.btn {
    background-color: #0066cc;
    color: white;
    padding: 10px 20px;
    text-decoration: none;
    margin: 5px;
    display: inline-block;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}

form label {
    display: block;
    margin-top: 10px;
}

form input, form select {
    width: 100%;
    padding: 8px;
    margin-top: 5px;
}

form input[type="submit"] {
    background-color: #0066cc;
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
}
document.addEventListener("DOMContentLoaded", function() {
    const params = new URLSearchParams(window.location.search);
    const curso = params.get('curso');
    
    if (curso) {
        const contenidoCurso = document.getElementById('contenido-curso');
        let contenido = '';

        if (curso === 'electricidad') {
            contenido = `
                <h2>Curso de Electricidad</h2>
                <p>Detalles sobre el curso de electricidad...</p>
                <ul>
                    <li>Módulo 1: Fundamentos de Electricidad</li>
                    <li>Módulo 2: Instalaciones Eléctricas Básicas</li>
                    <li>Módulo 3: Sistemas de Cableado y Conexiones</li>
                    <!-- Agrega más módulos según sea necesario -->
                </ul>
                <p>Costo: $100</p>
                <a href="registro.html" class="btn">Inscribirse Ahora</a>
            `;
        } else if (curso === 'refrigeracion') {
            contenido = `
                <h2>Curso de Refrigeración</h2>
                <p>Detalles sobre el curso de refrigeración...</p>
                <ul>
                    <li>Módulo 1: Principios de Refrigeración</li>
                    <li>Módulo 2: Manejo de Equipos de Refrigeración</li>
                    <li>Módulo 3: Mantenimiento y Reparación</li>
                    <!-- Agrega más módulos según sea necesario -->
                </ul>
                <p>Costo: $100</p>
                <a href="registro.html" class="btn">Inscribirse Ahora</a>
            `;
        }

        contenidoCurso.innerHTML = contenido;
    }
});
