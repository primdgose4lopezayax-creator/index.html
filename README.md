<!DOCTYPE html>
<html lang="es-MX">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Folleto Digital - Celerino Cano Palacio</title>
    <!-- Fuentes de Google -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,700&family=Inter:wght@300;400;600;700&family=Great+Vibes&display=swap" rel="stylesheet">
    <!-- Font Awesome 6 (Gratuito) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* ---------- RESET Y ESTILOS GLOBALES ---------- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #fcf9f5;
            color: #2c3e50;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* ---------- CONTENEDOR PRINCIPAL ---------- */
        .folio-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        /* ---------- SECCIÓN PORTADA ---------- */
        .portada {
            min-height: 90vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 40px 20px;
            background: linear-gradient(145deg, #fdf8f0 0%, #f0e6d3 100%);
            border-radius: 32px;
            margin-bottom: 40px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.05);
            animation: fadeInUp 1s ease-out forwards;
            opacity: 0;
            transform: translateY(30px);
        }

        @keyframes fadeInUp {
            to { opacity: 1; transform: translateY(0); }
        }

        .escudo {
            width: 130px;
            height: auto;
            margin-bottom: 20px;
            filter: drop-shadow(0 8px 12px rgba(0,0,0,0.15));
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-8px); }
        }

        .nombre-escuela {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2.2rem, 8vw, 4.5rem);
            font-weight: 700;
            color: #1a2a3a;
            letter-spacing: 1px;
            margin-bottom: 10px;
        }

        .lema {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1rem, 3vw, 1.8rem);
            font-weight: 400;
            font-style: italic;
            color: #8b6f4c;
            margin-bottom: 12px;
        }

        .anio {
            font-size: clamp(1rem, 2.5vw, 1.5rem);
            font-weight: 300;
            color: #5a6b7a;
            letter-spacing: 6px;
            text-transform: uppercase;
            border-top: 2px solid #d4c5a9;
            padding-top: 15px;
            display: inline-block;
        }

        .decoracion-portada {
            margin-top: 30px;
            display: flex;
            gap: 20px;
            font-size: 1.8rem;
            color: #b8a58c;
        }

        /* ---------- SECCIÓN CUERPO (CARRUSEL) ---------- */
        .cuerpo {
            margin: 30px 0 50px;
            position: relative;
        }

        .carrusel-wrapper {
            position: relative;
            overflow: hidden;
            border-radius: 28px;
            box-shadow: 0 12px 30px rgba(0,0,0,0.07);
            background-color: #ffffff;
            min-height: 550px;
        }

        .carrusel-track {
            display: flex;
            transition: transform 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            will-change: transform;
        }

        .diapositiva {
            flex: 0 0 100%;
            padding: 40px 45px;
            min-height: 550px;
            background: #ffffff;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        /* Tipografía dentro del carrusel */
        .diapositiva h2 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.6rem, 4vw, 2.8rem);
            color: #1a2a3a;
            margin-bottom: 18px;
            font-weight: 700;
            line-height: 1.2;
        }

        .diapositiva h2 i {
            color: #b8a58c;
            margin-right: 12px;
            font-size: 0.9em;
        }

        .diapositiva h3 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.2rem, 2.5vw, 1.8rem);
            color: #3d4f5e;
            margin: 20px 0 10px;
            font-weight: 600;
        }

        .diapositiva h3 i {
            color: #a78b6e;
            margin-right: 10px;
        }

        .diapositiva p, .diapositiva li {
            font-size: clamp(0.95rem, 1.3vw, 1.1rem);
            color: #34495e;
            margin-bottom: 12px;
            line-height: 1.7;
        }

        .diapositiva ul {
            list-style: none;
            padding-left: 0;
        }

        .diapositiva ul li {
            padding-left: 28px;
            position: relative;
            margin-bottom: 10px;
        }

        .diapositiva ul li::before {
            content: "▹";
            position: absolute;
            left: 4px;
            color: #a78b6e;
            font-weight: 700;
        }

        .grid-2col {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin: 15px 0;
        }

        /* Estilo para las barras de progreso */
        .logro-item {
            margin: 20px 0;
        }

        .logro-item .label {
            display: flex;
            justify-content: space-between;
            font-weight: 600;
            font-size: 0.95rem;
            color: #1a2a3a;
            margin-bottom: 6px;
        }

        .barra-fondo {
            width: 100%;
            height: 12px;
            background-color: #ece6dc;
            border-radius: 30px;
            overflow: hidden;
        }

        .barra-lleno {
            height: 100%;
            width: 0%;
            background: linear-gradient(90deg, #b8a58c, #8b6f4c);
            border-radius: 30px;
            transition: width 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        /* Controles del carrusel */
        .carrusel-controles {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 18px;
            margin-top: 22px;
        }

        .carrusel-controles button {
            background: #ffffff;
            border: 1.5px solid #d4c5a9;
            width: 48px;
            height: 48px;
            border-radius: 50%;
            font-size: 1.4rem;
            color: #5a4a3a;
            cursor: pointer;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 8px rgba(0,0,0,0.04);
        }

        .carrusel-controles button:hover {
            background: #8b6f4c;
            color: white;
            border-color: #8b6f4c;
            transform: scale(1.05);
        }

        .indicadores {
            display: flex;
            gap: 10px;
        }

        .indicador {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #d4c5a9;
            cursor: pointer;
            transition: all 0.3s;
            border: none;
        }

        .indicador.activo {
            background: #8b6f4c;
            transform: scale(1.2);
            box-shadow: 0 0 0 3px rgba(139, 111, 76, 0.2);
        }

        /* ---------- SECCIÓN DESPEDIDA ---------- */
        .despedida {
            background: linear-gradient(145deg, #f5efe7, #e8dfd2);
            border-radius: 32px;
            padding: 50px 45px;
            margin: 20px 0 30px;
            box-shadow: 0 12px 30px rgba(0,0,0,0.05);
            animation: fadeInUp 1s ease-out forwards;
            opacity: 0;
            transform: translateY(30px);
            animation-delay: 0.2s;
        }

        .despedida h2 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.8rem, 4vw, 2.8rem);
            color: #1a2a3a;
            margin-bottom: 20px;
            font-weight: 700;
        }

        .despedida .mensaje {
            font-size: clamp(1rem, 1.3vw, 1.15rem);
            color: #2c3e50;
            line-height: 1.8;
            margin-bottom: 25px;
            columns: 2 300px;
            column-gap: 40px;
        }

        .despedida .mensaje p {
            margin-bottom: 18px;
            break-inside: avoid;
        }

        .despedida .gracias {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2.5rem, 6vw, 4rem);
            font-weight: 700;
            font-style: italic;
            color: #8b6f4c;
            text-align: center;
            letter-spacing: 8px;
            margin: 20px 0 15px;
        }

        .firma {
            text-align: right;
            margin-top: 20px;
            padding-top: 25px;
            border-top: 2px solid #d4c5a9;
        }

        .firma .nombre {
            font-family: 'Great Vibes', cursive;
            font-size: clamp(2rem, 4vw, 3rem);
            color: #1a2a3a;
            line-height: 1.2;
        }

        .firma .cargo {
            font-size: 1rem;
            font-weight: 300;
            color: #5a6b7a;
            letter-spacing: 2px;
        }

        .fecha {
            text-align: right;
            font-weight: 300;
            color: #6a7b8a;
            font-size: 1rem;
            margin-top: 12px;
        }

        /* ---------- RESPONSIVE ---------- */
        @media (max-width: 768px) {
            .folio-container {
                padding: 12px;
            }

            .diapositiva {
                padding: 30px 24px;
                min-height: 480px;
            }

            .grid-2col {
                grid-template-columns: 1fr;
                gap: 10px;
            }

            .despedida {
                padding: 30px 22px;
            }

            .despedida .mensaje {
                columns: 1;
            }

            .carrusel-controles button {
                width: 42px;
                height: 42px;
                font-size: 1.2rem;
            }

            .portada {
                min-height: 70vh;
                padding: 30px 15px;
            }

            .escudo {
                width: 100px;
            }
        }

        @media (max-width: 480px) {
            .diapositiva {
                padding: 20px 16px;
                min-height: 420px;
            }

            .carrusel-controles {
                gap: 12px;
            }
        }

        /* Utilidades */
        .text-center { text-align: center; }
        .mt-1 { margin-top: 10px; }
        .mb-1 { margin-bottom: 10px; }
        .color-secundario { color: #8b6f4c; }
        .fw-300 { font-weight: 300; }
    </style>
</head>
<body>

<div class="folio-container">

    <!-- ==================== PORTADA ==================== -->
    <section class="portada" id="portada">
        <img class="escudo" src="https://lh3.googleusercontent.com/a-/ALV-UjVwwf1TvGki3EwJPTjA13XQk9OXVHNs6FhUFIiE4J-eDnD8w5I=s360-p-k-rw-no" alt="Escudo Celerino Cano Palacio">
        <h1 class="nombre-escuela">Celerino Cano Palacio</h1>
        <p class="lema">« Educando forjaremos un México mejor »</p>
        <span class="anio">Ciclo escolar 2025 - 2026</span>
        <div class="decoracion-portada">
            <i class="fas fa-graduation-cap"></i>
            <i class="fas fa-book-open"></i>
            <i class="fas fa-globe-americas"></i>
        </div>
    </section>

    <!-- ==================== CUERPO (CARRUSEL) ==================== -->
    <section class="cuerpo" id="cuerpo">

        <div class="carrusel-wrapper">
            <div class="carrusel-track" id="carruselTrack">

                <!-- D I A P O S I T I V A   1 -->
                <div class="diapositiva">
                    <h2><i class="fas fa-handshake"></i> Rumbo a una Convivencia Armónica</h2>
                    <p><strong>El inglés como Herramienta Comunitaria</strong></p>
                    <p>Al inicio de este ciclo escolar, el diagnóstico grupal nos señaló una ruta clara: era fundamental fortalecer las dinámicas de convivencia y los valores dentro de nuestra comunidad escolar. Con este propósito en mente, diseñamos y pusimos en marcha <strong>7 proyectos clave</strong> dirigidos a los grupos de 1°, 2°, 3° y 4° de primaria.</p>
                    <p>Nuestra estrategia pedagógica no se limitó a la teoría; buscamos exponer a los estudiantes a un lenguaje real y vivo mediante el uso de herramientas digitales como videos, canciones y búsquedas guiadas en línea. De este modo, logramos que el aprendizaje del inglés fuera el vehículo perfecto para conectar los Procesos de Desarrollo de Aprendizaje (PDA) con la práctica diaria de valores esenciales, transformando el idioma en una herramienta formativa que impacta positivamente en el bienestar común y en el desarrollo integral de sus hijos.</p>
                </div>

                <!-- D I A P O S I T I V A   2 -->
                <div class="diapositiva">
                    <h2><i class="fas fa-laptop"></i> Conectando con el Mundo Digital</h2>
                    <p><strong>El inglés más allá del aula.</strong></p>
                    <ul>
                        <li><strong>¿Qué logramos?</strong> Diseñamos 7 proyectos pedagógicos donde los alumnos no se limitaron a repetir palabras de un libro, sino que se convirtieron en investigadores.</li>
                        <li><strong>La estrategia:</strong> Expusimos a los estudiantes a fuentes de lenguaje real mediante videos, canciones interactivas y búsquedas guiadas en internet (online). Esto les permitió desarrollar el oído, adquirir vocabulario auténtico y entender cómo se usa el idioma en el día a día a nivel global.</li>
                    </ul>

                    <h3><i class="fas fa-arrow-right"></i> Progresión de Aprendizajes por Grado (PDA)</h3>
                    <p><strong>¿Cómo avanzó cada nivel?</strong> A través de nuestros 7 proyectos, los contenidos se adaptaron minuciosamente al ritmo y madurez de cada grupo:</p>
                    <div class="grid-2col">
                        <div>
                            <h4 style="color:#5a4a3a; font-weight:600;">1° y 2° Grado</h4>
                            <p><strong>Familiarización y Expresión Básica:</strong> Los más pequeños consolidaron su capacidad para escuchar, identificar sonidos clave, cantar y responder a instrucciones sencillas en inglés mediante contenido audiovisual interactivo.</p>
                        </div>
                        <div>
                            <h4 style="color:#5a4a3a; font-weight:600;">3° y 4° Grado</h4>
                            <p><strong>Investigación y Uso Activo:</strong> Los alumnos mayores avanzaron hacia la búsqueda de información específica en entornos digitales, la lectura de textos breves y la expresión de ideas propias utilizando herramientas tecnológicas.</p>
                        </div>
                    </div>
                </div>

                <!-- D I A P O S I T I V A   3 -->
                <div class="diapositiva">
                    <h2><i class="fas fa-heart"></i> Idioma con Propósito: Formación en Valores</h2>
                    <p><strong>Aprender inglés para ser mejores ciudadanos.</strong></p>
                    <ul>
                        <li><strong>Del diagnóstico a la acción:</strong> Al inicio del ciclo escolar identificamos que las dinámicas de convivencia y la vida en comunidad eran un área de mejora prioritaria.</li>
                        <li><strong>Nuestra respuesta:</strong> No solo enseñamos gramática; usamos cada proyecto de inglés como un vehículo para reflexionar y poner en práctica valores fundamentales. Los materiales digitales seleccionados (videos y lecturas) promovieron activamente la empatía, el respeto, el trabajo en equipo y la resolución pacífica de conflictos.</li>
                    </ul>

                    <h3><i class="fas fa-chart-line"></i> Resultados: El Impacto en nuestra Comunidad</h3>
                    <p><strong>¿Qué nos dejan estos 7 proyectos?</strong> Al cerrar el ciclo escolar, el balance es sumamente positivo. Gracias a la combinación de tecnología, lenguaje real y enfoque humano, logramos:</p>
                    <ul>
                        <li><strong>Mayor motivación:</strong> Alumnos que disfrutan aprender inglés a través de la música y la tecnología.</li>
                        <li><strong>Habilidades digitales:</strong> Estudiantes más críticos al buscar información en la red.</li>
                        <li><strong>Ambiente escolar armónico:</strong> Una mejora notable en las dinámicas de grupo, el respeto mutuo y la colaboración comunitaria dentro y fuera del salón de clases.</li>
                    </ul>
                </div>

                <!-- D I A P O S I T I V A   4 (LOGROS CUANTITATIVOS) -->
                <div class="diapositiva">
                    <h2><i class="fas fa-trophy"></i> Logros del Ciclo Escolar</h2>
                    <p style="font-weight:300; margin-bottom:25px;">Resultados cuantitativos que reflejan el impacto de nuestra metodología.</p>

                    <div class="logro-item">
                        <div class="label">
                            <span>Percepción auditiva y producción fonética</span>
                            <span>+80%</span>
                        </div>
                        <div class="barra-fondo">
                            <div class="barra-lleno" data-porcentaje="80"></div>
                        </div>
                        <p style="font-size:0.85rem; color:#5a6b7a; margin-top:4px;">Identifican sonidos del inglés y los incorporan a su habla.</p>
                    </div>

                    <div class="logro-item">
                        <div class="label">
                            <span>Uso del inglés para intercambios académicos</span>
                            <span>+60%</span>
                        </div>
                        <div class="barra-fondo">
                            <div class="barra-lleno" data-porcentaje="60"></div>
                        </div>
                        <p style="font-size:0.85rem; color:#5a6b7a; margin-top:4px;">Pueden utilizar el idioma para obtener información académica.</p>
                    </div>

                    <div class="logro-item">
                        <div class="label">
                            <span>Fase 4: Precisión contextual</span>
                            <span>+60%</span>
                        </div>
                        <div class="barra-fondo">
                            <div class="barra-lleno" data-porcentaje="60"></div>
                        </div>
                        <p style="font-size:0.85rem; color:#5a6b7a; margin-top:4px;">Reconocen y responden a frases cotidianas con alto nivel de comprensión.</p>
                    </div>

                    <div class="logro-item">
                        <div class="label">
                            <span>Fase 5: Presentaciones académicas en inglés</span>
                            <span>+60%</span>
                        </div>
                        <div class="barra-fondo">
                            <div class="barra-lleno" data-porcentaje="60"></div>
                        </div>
                        <p style="font-size:0.85rem; color:#5a6b7a; margin-top:4px;">Capaces de presentar material académico usando solo inglés y producciones propias.</p>
                    </div>
                </div>

            </div> <!-- fin carrusel-track -->
        </div> <!-- fin carrusel-wrapper -->

        <!-- Controles del carrusel -->
        <div class="carrusel-controles">
            <button id="btnAnterior" aria-label="Diapositiva anterior"><i class="fas fa-chevron-left"></i></button>
            <div class="indicadores" id="indicadores">
                <span class="indicador activo" data-index="0"></span>
                <span class="indicador" data-index="1"></span>
                <span class="indicador" data-index="2"></span>
                <span class="indicador" data-index="3"></span>
            </div>
            <button id="btnSiguiente" aria-label="Diapositiva siguiente"><i class="fas fa-chevron-right"></i></button>
        </div>

    </section>

    <!-- ==================== DESPEDIDA ==================== -->
    <section class="despedida" id="despedida">
        <h2><i class="fas fa-envelope-open-text" style="color:#8b6f4c; margin-right:12px;"></i> Mensaje de Cierre</h2>
        <div class="mensaje">
            <p>Ha sido un verdadero honor y un privilegio acompañar a sus hijos en este ciclo escolar, siendo testigo diario de su curiosidad, su esfuerzo y las ganas de salir adelante que nutren nuestra aula. El éxito de este periodo y los logros alcanzados son el resultado directo de un trabajo en equipo; por ello, agradezco profundamente la confianza y el respaldo incondicional que ustedes, como familias, han brindado a mi labor desde casa. Me despido de este periodo con el corazón lleno de gratitud y con el firme entusiasmo de continuar colaborando estrechamente con esta maravillosa comunidad escolar, esperando tener la oportunidad de seguir impulsando el trayecto formativo de los estudiantes, potenciando sus habilidades académicas y apoyando su crecimiento como seres humanos extraordinarios.</p>
            <p>Concluir este periodo nos invita a reflexionar sobre el camino recorrido, donde ver crecer a los alumnos, superar retos y descubrir su potencial ha sido una experiencia sumamente gratificante y enriquecedora. Trabajar de la mano con cada uno de ustedes ha permitido consolidar un esfuerzo compartido que fortalece el bienestar de nuestra comunidad educativa. Mantengo el compromiso absoluto de seguir sumando esfuerzos en la guía de sus hijos, con la sincera expectativa de continuar contribuyendo a su evolución académica y personal en las etapas venideras, siempre apostando por su excelencia y desarrollo integral.</p>
        </div>

        <div class="gracias">GRACIAS</div>

        <div class="firma">
            <div class="nombre">Ayax López Valdés</div>
            <div class="cargo">Profesor de Inglés</div>
        </div>
        <div class="fecha">Julio 2026</div>
    </section>

</div> <!-- fin folio-container -->

<!-- ==================== JAVASCRIPT ==================== -->
<script>
    document.addEventListener('DOMContentLoaded', function() {

        // ---- CARRUSEL ----
        const track = document.getElementById('carruselTrack');
        const diapositivas = track.querySelectorAll('.diapositiva');
        const total = diapositivas.length;
        let indiceActual = 0;

        const btnAnterior = document.getElementById('btnAnterior');
        const btnSiguiente = document.getElementById('btnSiguiente');
        const indicadores = document.querySelectorAll('.indicador');

        function actualizarCarrusel(index) {
            if (index < 0) index = total - 1;
            if (index >= total) index = 0;
            indiceActual = index;
            const desplazamiento = -indiceActual * 100;
            track.style.transform = `translateX(${desplazamiento}%)`;

            // Actualizar indicadores
            indicadores.forEach((dot, i) => {
                dot.classList.toggle('activo', i === indiceActual);
            });
        }

        btnSiguiente.addEventListener('click', function() {
            actualizarCarrusel(indiceActual + 1);
        });

        btnAnterior.addEventListener('click', function() {
            actualizarCarrusel(indiceActual - 1);
        });

        indicadores.forEach((dot) => {
            dot.addEventListener('click', function() {
                const index = parseInt(this.getAttribute('data-index'));
                actualizarCarrusel(index);
            });
        });

        // ---- BARRAS DE PROGRESO (con Intersection Observer) ----
        const barras = document.querySelectorAll('.barra-lleno');
        let observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const barra = entry.target;
                    const porcentaje = parseFloat(barra.getAttribute('data-porcentaje'));
                    if (porcentaje > 0 && barra.style.width === '0%' || barra.style.width === '') {
                        // Asignar el ancho después de un pequeño retraso para que la transición sea visible
                        setTimeout(() => {
                            barra.style.width = porcentaje + '%';
                        }, 150);
                    }
                }
            });
        }, { threshold: 0.3 });

        barras.forEach(barra => observer.observe(barra));

        // Si alguna barra ya está visible al cargar, se activa
        barras.forEach(barra => {
            const rect = barra.closest('.diapositiva').getBoundingClientRect();
            if (rect.top < window.innerHeight && rect.bottom > 0) {
                // Pequeño retraso para que el observer también dispare
                setTimeout(() => {
                    const porcentaje = parseFloat(barra.getAttribute('data-porcentaje'));
                    if (porcentaje > 0 && barra.style.width === '0%' || barra.style.width === '') {
                        barra.style.width = porcentaje + '%';
                    }
                }, 300);
            }
        });

        // ---- KEYBOARD NAVEGACIÓN (accesibilidad) ----
        document.addEventListener('keydown', (e) => {
            if (e.key === 'ArrowRight') {
                e.preventDefault();
                actualizarCarrusel(indiceActual + 1);
            } else if (e.key === 'ArrowLeft') {
                e.preventDefault();
                actualizarCarrusel(indiceActual - 1);
            }
        });

    });
</script>

</body>
</html>
