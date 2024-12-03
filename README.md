<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Taller GA1-220501092-AA3-EV03</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            background-color: #f9f9f9;
        }
        h1, h2, h3 {
            text-align: center;
            color: #333;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        .section {
            background: #fff;
            margin: 20px 0;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .toc {
            margin: 20px 0;
            padding: 20px;
            background: #e6f7ff;
            border-radius: 8px;
        }
        .toc a {
            display: block;
            margin: 5px 0;
            color: #0066cc;
            text-decoration: none;
        }
        .toc a:hover {
            text-decoration: underline;
        }
        .chart-container {
            width: 100%;
            max-width: 600px;
            margin: 0 auto;
        }
        ul {
            padding-left: 20px;
        }
        .analysis {
            margin-top: 15px;
        }
        .analysis strong {
            display: block;
            margin-bottom: 10px;
        }
        .credits {
            text-align: center;
            margin: 20px 0;
            font-size: 14px;
            color: #555;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Taller GA1-220501092-AA3-EV03</h1>
        <h2>Academia TurboDrive</h2>
        <p class="credits">
            <strong>Integrantes del Grupo:</strong><br>
            Kevin Alexander Montoya Valdez<br>
            Viviana Edith Cepeda Pérez<br>
            Néstor Hernán Gallo Jiménez<br>
            Ingrid Yamile Méndez Cárdenas<br><br>
            <strong>Instructor:</strong> Alexander Calderón Martínez<br><br>
            <strong>Institución:</strong> Servicio Nacional de Aprendizaje SENA<br>
            Centro Agropecuario La Granja - Regional Tolima<br><br>
            <strong>Programa:</strong> Análisis y Desarrollo de Software<br>
            Ficha (3070453)<br>
            Noviembre 2024
        </p>

        <!-- Tabla de contenido -->
        <div class="toc">
            <h3>Tabla de Contenido</h3>
            <a href="#introduccion">1. Introducción</a>
            <a href="#diseno-instrumento">2. Diseño del Instrumento</a>
            <a href="#resultados">3. Análisis de Resultados</a>
            <a href="#interpretacion">4. Interpretación de los Resultados</a>
            <a href="#conclusiones">5. Conclusiones</a>
        </div>

        <!-- Introducción -->
        <div id="introduccion" class="section">
            <h3>1. Introducción</h3>
            <p>
                El presente trabajo se centra en la creación de un instrumento de recolección de datos que permita analizar 
                las necesidades y expectativas de los usuarios de la plataforma educativa de la Academia TurboDrive. La 
                finalidad es desarrollar un software eficiente, moderno y adaptable a los distintos perfiles de usuarios.
            </p>
        </div>

        <!-- Diseño del Instrumento -->
        <div id="diseno-instrumento" class="section">
            <h3>2. Diseño del Instrumento</h3>
            <p>La encuesta se desarrolló teniendo en cuenta los siguientes aspectos:</p>
            <ul>
                <li><strong>Sección 1:</strong> Datos Generales. Identifica el perfil del usuario y su experiencia tecnológica.</li>
                <li><strong>Sección 2:</strong> Funcionalidades y Usabilidad. Evalúa la importancia de características clave.</li>
                <li><strong>Sección 3:</strong> Experiencia del Usuario. Mide la intuitividad, accesibilidad y diseño.</li>
                <li><strong>Sección 4:</strong> Innovaciones Tecnológicas. Explora preferencias sobre autenticación y herramientas avanzadas.</li>
            </ul>
        </div>

        <!-- Análisis de Resultados -->
        <div id="resultados" class="section">
            <h3>3. Análisis de Resultados</h3>
            <p>Los resultados de las encuestas se presentan mediante gráficos visuales e interpretaciones detalladas:</p>

            <!-- Gráfico de barras -->
            <div class="chart-container">
                <canvas id="barChart"></canvas>
            </div>

            <div class="analysis">
                <strong>Resultados destacados:</strong>
                <ul>
                    <li>El 80% de los usuarios considera esencial el registro de estudiantes.</li>
                    <li>El diseño intuitivo es la prioridad más alta, con un 90% de preferencia.</li>
                    <li>Las notificaciones automáticas tienen un interés del 65%, reflejando su importancia.</li>
                </ul>
            </div>

            <!-- Gráfico de pastel -->
            <div class="chart-container">
                <canvas id="pieChart"></canvas>
            </div>
        </div>

        <!-- Interpretación de Resultados -->
        <div id="interpretacion" class="section">
            <h3>4. Interpretación de los Resultados</h3>
            <p>
                Los resultados confirman que la prioridad de los usuarios está en características que faciliten la gestión, como 
                el registro de estudiantes y las notificaciones automáticas. La importancia del diseño intuitivo destaca la necesidad 
                de interfaces accesibles para diferentes perfiles de usuarios.
            </p>
        </div>

        <!-- Conclusiones -->
        <div id="conclusiones" class="section">
            <h3>5. Conclusiones</h3>
            <p>
                La encuesta permitió recopilar información esencial para guiar el diseño del software educativo. Las conclusiones 
                más relevantes incluyen:
            </p>
            <ul>
                <li>La necesidad de un diseño intuitivo y accesible para todos los usuarios.</li>
                <li>La prioridad de funcionalidades organizativas como registro de estudiantes y cronogramas.</li>
                <li>La importancia de tecnologías de seguridad avanzadas como autenticación en dos pasos.</li>
            </ul>
        </div>
    </div>

    <!-- Gráficos con Chart.js -->
    <script>
        const barCtx = document.getElementById('barChart').getContext('2d');
        const barChart = new Chart(barCtx, {
            type: 'bar',
            data: {
                labels: ['Registro de Estudiantes', 'Cronograma de Clases', 'Notificaciones', 'Soporte Técnico', 'Diseño Intuitivo'],
                datasets: [{
                    label: 'Preferencias de Funcionalidades (%)',
                    data: [80, 70, 65, 50, 90],
                    backgroundColor: [
                        'rgba(54, 162, 235, 0.7)',
                        'rgba(255, 99, 132, 0.7)',
                        'rgba(255, 206, 86, 0.7)',
                        'rgba(75, 192, 192, 0.7)',
                        'rgba(153, 102, 255, 0.7)'
                    ],
                    borderColor: [
                        'rgba(54, 162, 235, 1)',
                        'rgba(255, 99, 132, 1)',
                        'rgba(255, 206, 86, 1)',
                        'rgba(75, 192, 192, 1)',
                        'rgba(153, 102, 255, 1)'
                    ],
                    borderWidth: 1
                }]
            },
            options: {
                scales: {
                    y: {
                        beginAtZero: true,
                        max: 100
                    }
                }
            }
        });

        const pieCtx = document.getElementById('pieChart').getContext('2d');
        const pieChart = new Chart(pieCtx, {
            type: 'pie',
            data: {
                labels: ['Contraseña Única', 'Verificación en Dos Pasos', 'Inicio con Correo'],
                datasets: [{
                    data: [40, 35, 25],
                    backgroundColor: [
                        'rgba(255, 99, 132, 0.7)',
                        'rgba(54, 162, 235, 0.7)',
                        'rgba(75, 192, 192, 0.7)'
                    ],
                    borderColor: [
                        'rgba(255, 99, 132, 1)',
                        'rgba(54, 162, 235, 1)',
                        'rgba(75, 192, 192, 1)'
                    ],
                    borderWidth: 1
                }]
            },
            options: {
                plugins: {
                    legend: {
                        position: 'top',
                    }
                }
            }
        });
    </script>
</body>
</html>
