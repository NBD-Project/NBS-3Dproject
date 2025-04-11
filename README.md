# NBS-3Dproject
Modelado 3d, textura, diseño y animaciòn
<!DOCTYPE html>
<html>
  </head>
<body>
<head>
   
    <title>Explorando el Mundo del 3D</title>
</head>


    <header>
        <h1>Explorando el Mundo del 3D</h1>
    </header>

    <div class="content">
        <h2>¿Qué es el 3D?</h2>
        <p>El 3D, o tres dimensiones, es una representación visual de objetos que tiene profundidad, alto y ancho, a diferencia de las imágenes 2D, que solo muestran alto y ancho. El 3D permite crear figuras y escenas realistas que se pueden ver desde diferentes ángulos, lo que facilita la interacción y la inmersión. 3D significa "tres dimensiones": alto, ancho y profundidad. A diferencia de una imagen plana (2D), un objeto 3D tiene volumen y puede rotarse o verse desde distintos ángulos.<br>

<br>
El modelado 3D es el proceso de crear representaciones digitales de objetos en tres dimensiones, utilizando software especializado. Este proceso se utiliza en áreas como cine, videojuegos, arquitectura y medicina.<br>
<br>
Malla: Es la estructura básica de un objeto 3D, formada por vértices, aristas y caras.<br>
<br>
Texturización: Aplicación de imágenes sobre la superficie de los modelos para darles realismo.<br>
<br>
Rigging y Animación: Creación de esqueletos dentro de los modelos 3D para darles movimiento.<br>
<br>
Renderizado: Proceso de generar una imagen 2D a partir de un modelo 3D, simulando la interacción de la luz.
</p>

        <h2>¿Cómo se crean los gráficos 3D?</h2>
        <p>Los gráficos 3D se crean utilizando software especializado que permite modelar, iluminar y texturizar objetos. Además, se usan tecnologías como:</p>
        <ul>
            <li><strong>Modelado 3D:</strong> Proceso de crear formas en tres dimensiones.</li>
            <li><strong>Animación 3D:</strong> Se da movimiento a los objetos modelados.</li>
            <li><strong>Renderización:</strong> El proceso de generar imágenes realistas o estilizadas a partir de los modelos 3D.</li>
            <li><strong>Realidad Virtual (VR):</strong> Utiliza gráficos 3D para crear experiencias inmersivas en entornos virtuales.</li>
        </ul>

        <h2>Gráfico de un Cubo en 3D</h2>
        <p>En esta página puedes ver un cubo 3D que rota constantemente.</p>

        <div class="cubo-container">
            <div class="cubo">
                <div class="cara frente"></div>
                <div class="cara atras"></div>
                <div class="cara izquierda"></div>
                <div class="cara derecha"></div>
                <div class="cara arriba"></div>
                <div class="cara abajo"></div>
            </div>
        </div>

        <h3>Aplicaciones del 3D</h3>
        <p>Las aplicaciones del 3D son vastas y se encuentran en muchos campos como:</p>
        <ul>
            <li><strong>Cine y Entretenimiento:</strong> Animación y efectos especiales en películas y videojuegos.</li>
            <li><strong>Medicina:</strong> Visualización de órganos y estructuras internas para diagnósticos.</li>
            <li><strong>Arquitectura:</strong> Modelado y visualización de edificios y paisajes urbanos.</li>
            <li><strong>Educación:</strong> Creación de simulaciones interactivas y visualizaciones en 3D.</li>
        </ul>

        <h3>Conclusión</h3>
        <p>El mundo del 3D ha revolucionado la manera en que interactuamos con los medios digitales. A medida que la tecnología avanza, el 3D continúa siendo una herramienta poderosa para crear experiencias inmersivas y visualizaciones detalladas en una variedad de campos.</p>
    </div>

    <footer>
        <p>Creado por Etzel Escalante, Natalie Trujillo, Isabella Sandoval & Alec Galindo. Todos los derechos reservados.</p>
    </footer>

</body>

</html>


<Código de cubo 3d

index.html

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página Web 3D</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <div class="cubo" id="cubo">
            <div class="cara frente"></div>
            <div class="cara atras"></div>
            <div class="cara izquierda"></div>
            <div class="cara derecha"></div>
            <div class="cara arriba"></div>
            <div class="cara abajo"></div>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>

styles.css

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body, html {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #f0f0f0;
}

.container {
    perspective: 600px;
}

.cubo {
    width: 200px;
    height: 200px;
    position: relative;
    transform-style: preserve-3d;
    transform: rotateX(0deg) rotateY(0deg);
    animation: rotar 5s infinite linear;
}

.cara {
    position: absolute;
    width: 200px;
    height: 200px;
    background-color: rgba(0, 150, 255, 0.8);
    border: 2px solid #000;
}

.frente  { transform: translateZ(100px); }
.atras   { transform: rotateY(180deg) translateZ(100px); }
.izquierda { transform: rotateY(-90deg) translateZ(100px); }
.derecha { transform: rotateY(90deg) translateZ(100px); }
.arriba  { transform: rotateX(90deg) translateZ(100px); }
.abajo   { transform: rotateX(-90deg) translateZ(100px); }

@keyframes rotar {
    0% { transform: rotateX(0deg) rotateY(0deg); }
    100% { transform: rotateX(360deg) rotateY(360deg); }

