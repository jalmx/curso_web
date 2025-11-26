# Ejercicios

## HTML

1. Realizar un pagina web de una sola pagina, para una tienda de componentes electronicos, nombre la empresa "Super transistor". las secciones internas son
      1. Barra de navegación con los enlaces a cada sección (con # y ids en los títulos y subtítulos)
      2. Titulo del sitio
      3. imagen para el header que ocupe el 100% del ancho, que sea una imagen rectangular no muy alta
      4. sección uno: Su Titulo, Description de lo que venden (texto dummy unos 3 párrafos de contenido)
      5. sección dos: su Titulo: agrega una lista ordenada con unos 10 componentes electronicos, debajo agrega 5 fotos de componentes que entren en el ancho de la pantalla, no se deben desbordar.
      6.Footer: Agregar la misma navegación para que ir rápido al inicio y a cada sección, agregar un correo de contacto y un numero de contacto (mailto: y tel:+)

??? example "Ejemplo código"

    ```html
    <!DOCTYPE html>
    <html lang="es">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Super Transistor - Componentes Electrónicos</title>
    </head>
    <body>
        <!-- Barra de Navegación -->
        <nav>
            <ul>
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#productos">Productos</a></li>
                <li><a href="#componentes">Componentes</a></li>
            </ul>
        </nav>

        <!-- Título del Sitio -->
        <header id="inicio">
            <h1>Super Transistor</h1>
            <img src="images/header-electronica.jpg" alt="Componentes electrónicos y herramientas" width="100%">
        </header>

        <!-- Sección 1: Descripción -->
        <section id="productos">
            <h2>Nuestros Productos Electrónicos</h2>
            <p>Primer párrafo de descripción sobre los componentes electrónicos que vendemos...</p>
            <p>Segundo párrafo explicando la calidad de nuestros productos y servicios...</p>
            <p>Tercer párrafo sobre nuestra experiencia en el mercado electrónico...</p>
        </section>

        <!-- Sección 2: Componentes -->
        <section id="componentes">
            <h2>Componentes Disponibles</h2>

            <!-- Lista ordenada de componentes -->
            <ol>
                <li>Resistores</li>
                <li>Capacitores electrolíticos</li>
                <li>Transistores NPN</li>
                <li>Transistores PNP</li>
                <li>Diodos LED</li>
                <li>Microcontroladores Arduino</li>
                <li>Circuitos integrados 555</li>
                <li>Reguladores de voltaje</li>
                <li>Conectores JST</li>
                <li>Placas PCB</li>
            </ol>

            <!-- Galería de imágenes -->
            <article>
                <img src="images/resistor.jpg" alt="Resistor electrónico" width="19%">
                <img src="images/capacitor.jpg" alt="Capacitor electrolítico" width="19%">
                <img src="images/transistor.jpg" alt="Transistor NPN" width="19%">
                <img src="images/led.jpg" alt="Diodo LED" width="19%">
                <img src="images/arduino.jpg" alt="Microcontrolador Arduino" width="19%">
            </article>
        </section>

        <!-- Footer -->
        <footer>
            <!-- Navegación rápida -->
            <nav>
                <ul>
                    <li><a href="#inicio">Volver al Inicio</a></li>
                    <li><a href="#productos">Nuestros Productos</a></li>
                    <li><a href="#componentes">Componentes</a></li>
                </ul>
            </nav>

            <!-- Información de contacto -->
            <p>
                Contacto:
                <a href="mailto:ventas@supertransistor.com">ventas@supertransistor.com</a> |
                <a href="tel:+573001234567">+57 300 123 4567</a>
            </p>
        </footer>
    </body>
    </html>
    ```

2\. Realizar una pagina web de varias páginas, para una empresa de venta de diseño de tarjetas electrónicas, nombre "PCBtronix"

   1. Barra de navegación en cada página, con los enlaces a cada página y sección interna (con # y ids en los títulos y subtítulos, para las secciones internas usa una lista ordenada, para enlazar las otras páginas colócalas en una lista sin orden)
   2. index.html: Título del negocio, párrafo de descripción (2 párrafos dummys) con una imagen debajo. Sección 1: Subtitulo "Nuestros Servicios" (id="servicios"), 3 párrafos dummy. Sección 2: Lista de servicios ofrecidos (lista ordenada). Sección 3: Ventajas Competitivas (id="ventajas") agrega 3 párrafos con información(dummy). Sección 4: Ventas y beneficios. Lista de 5 ventajas (lista ordenada) y 5 beneficios (lista no ordenada) [en la lista es texto dummy].
   3. catalogo.html: Título: "Catálogo de Tarjetas Electrónicas", agrega una imagen representativa. Sección 1 a la 5: subtitulo: "Componentes XXX", agregar 9 fotos en en cada sección, 3 fotos por linea.
   4. contacto.html: Título: "Contáctanos". Sección 1: Información de Contacto (id="informacion"), párrafo dummy, Dirección física completa, Teléfonos de contacto, Correo electrónico, Horarios de atención.
   5. quienes_somos.html: Título: "Conoce PCBtronix". Sección 1: Nuestra Historia (id="historia"), 2 Párrafos dummy con la información de la historia. Sección 2: "Perfiles", colocar una sección por perfil, cada perfil tendrá una nombre de la persona, una descripcion y una foto (eres libre como acomodarlo)

**Estructura del proyecto**

```text

pcbtronix/
├── index.html
├── catalogo.html
├── contacto.html
├── quienes_somos.html
├── header-pcb.jpg
├── catalogo-tarjetas.jpg
```

??? example "index.html"
    ```html
    <!DOCTYPE html>
    <html lang="es">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>PCBtronix - Diseño de Tarjetas Electrónicas</title>
    </head>
    <body>
        <!-- Barra de Navegación -->
        <nav>
            <!-- Lista SIN orden para páginas -->
            <ul>
                <li><a href="index.html">Inicio</a></li>
                <li><a href="catalogo.html">Catálogo</a></li>
                <li><a href="quienes_somos.html">Quiénes Somos</a></li>
                <li><a href="contacto.html">Contacto</a></li>
            </ul>

            <!-- Lista ordenada para secciones internas -->
            <ol>
                <li><a href="#servicios">Nuestros Servicios</a></li>
                <li><a href="#ventajas">Ventajas Competitivas</a></li>
            </ol>
        </nav>

        <!-- Título del negocio -->
        <h1>PCBtronix</h1>

        <!-- Descripción -->
        <p>Primer párrafo dummy describiendo PCBtronix y su especialización en diseño de tarjetas electrónicas...</p>
        <p>Segundo párrafo dummy explicando la experiencia y calidad de los servicios ofrecidos...</p>

        <!-- Imagen -->
        <img src="images/header-pcb.jpg" alt="Diseño de tarjetas electrónicas PCB" width="100%">

        <!-- Sección 1: Nuestros Servicios -->
        <section id="servicios">
            <h2>Nuestros Servicios</h2>
            <p>Primer párrafo dummy sobre servicios de diseño personalizado...</p>
            <p>Segundo párrafo dummy sobre fabricación y prototipado...</p>
            <p>Tercer párrafo dummy sobre soporte técnico y asesoría...</p>

            <!-- Lista ordenada de servicios -->
            <ol>
                <li>Diseño de circuitos personalizados</li>
                <li>Prototipado rápido de PCBs</li>
                <li>Análisis y optimización de circuitos</li>
            </ol>
        </section>

        <!-- Sección 2: Ventajas Competitivas -->
        <section id="ventajas">
            <h2>Ventajas Competitivas</h2>
            <p>Primer párrafo dummy sobre experiencia del equipo...</p>
            <p>Segundo párrafo dummy sobre tecnología de punta...</p>
            <p>Tercer párrafo dummy sobre tiempos de entrega...</p>

            <!-- Ventajas y beneficios -->
            <h3>Ventajas:</h3>
            <ol>
                <li>Ventaja 1 dummy</li>
                <li>Ventaja 2 dummy</li>
                <li>Ventaja 3 dummy</li>
                <li>Ventaja 4 dummy</li>
                <li>Ventaja 5 dummy</li>
            </ol>

            <h3>Beneficios:</h3>
            <ul>
                <li>Beneficio 1 dummy</li>
                <li>Beneficio 2 dummy</li>
                <li>Beneficio 3 dummy</li>
                <li>Beneficio 4 dummy</li>
                <li>Beneficio 5 dummy</li>
            </ul>
        </section>
    </body>
    </html>
    ```

??? example "catalogo.html"
    ```html
    <!DOCTYPE html>
    <html lang="es">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Catálogo - PCBtronix</title>
    </head>
    <body>
        <!-- Barra de Navegación -->
        <nav>
            <!-- Lista SIN orden para páginas -->
            <ul>
                <li><a href="index.html">Inicio</a></li>
                <li><a href="catalogo.html">Catálogo</a></li>
                <li><a href="quienes_somos.html">Quiénes Somos</a></li>
                <li><a href="contacto.html">Contacto</a></li>
            </ul>

            <!-- Lista ordenada para secciones internas -->
            <ol>
                <li><a href="#componentes1">Componentes Básicos</a></li>
                <li><a href="#componentes2">Microcontroladores</a></li>
                <li><a href="#componentes3">Sensores</a></li>
                <li><a href="#componentes4">Módulos de Comunicación</a></li>
                <li><a href="#componentes5">Herramientas y Accesorios</a></li>
            </ol>
        </nav>

        <!-- Título Principal -->
        <h1>Catálogo de Tarjetas Electrónicas</h1>

        <!-- Imagen Representativa -->
        <img src="images/catalogo-tarjetas.jpg" alt="Catálogo de tarjetas electrónicas PCBtronix" width="100%">

        <!-- Sección 1: Componentes Básicos -->
        <section id="componentes1">
            <h2>Componentes Básicos</h2>

            <!-- Línea 1 de 3 imágenes -->
            <div>
                <img src="resistores.jpg" alt="Resistores de precisión" width="32%">
                <img src="capacitores.jpg" alt="Capacitores electrolíticos" width="32%">
                <img src="transistores.jpg" alt="Transistores NPN y PNP" width="32%">
            </div>

            <!-- Línea 2 de 3 imágenes -->
            <div>
                <img src="diodos.jpg" alt="Diodos y LEDs" width="32%">
                <img src="inductores.jpg" alt="Inductores y bobinas" width="32%">
                <img src="cristales.jpg" alt="Cristales osciladores" width="32%">
            </div>

            <!-- Línea 3 de 3 imágenes -->
            <div>
                <img src="reguladores.jpg" alt="Reguladores de voltaje" width="32%">
                <img src="opamps.jpg" alt="Amplificadores operacionales" width="32%">
                <img src="connectors.jpg" alt="Conectores y headers" width="32%">
            </div>
        </section>

        <!-- Sección 2: Microcontroladores -->
        <section id="componentes2">
            <h2>Microcontroladores</h2>

            <!-- Línea 1 de 3 imágenes -->
            <div>
                <img src="arduino-uno.jpg" alt="Arduino UNO R3" width="32%">
                <img src="esp32.jpg" alt="ESP32 Dev Board" width="32%">
                <img src="raspberry-pi.jpg" alt="Raspberry Pi 4" width="32%">
            </div>

            <!-- Línea 2 de 3 imágenes -->
            <div>
                <img src="stm32.jpg" alt="STM32 Blue Pill" width="32%">
                <img src="attiny85.jpg" alt="ATtiny85" width="32%">
                <img src="pic16f877.jpg" alt="PIC16F877" width="32%">
            </div>

            <!-- Línea 3 de 3 imágenes -->
            <div>
                <img src="teensy.jpg" alt="Teensy 4.1" width="32%">
                <img src="nodemcu.jpg" alt="NodeMCU" width="32%">
                <img src="arduino-nano.jpg" alt="Arduino Nano" width="32%">
            </div>
        </section>

        <!-- Sección 3: Sensores -->
        <section id="componentes3">
            <h2>Sensores</h2>

            <!-- Línea 1 de 3 imágenes -->
            <div>
                <img src="temperatura.jpg" alt="Sensor de temperatura DHT22" width="32%">
                <img src="humedad.jpg" alt="Sensor de humedad suelo" width="32%">
                <img src="movimiento.jpg" alt="Sensor de movimiento PIR" width="32%">
            </div>

            <!-- Línea 2 de 3 imágenes -->
            <div>
                <img src="proximidad.jpg" alt="Sensor de proximidad ultrasonico" width="32%">
                <img src="luz.jpg" alt="Sensor de luz LDR" width="32%">
                <img src="gas.jpg" alt="Sensor de gas MQ-2" width="32%">
            </div>

            <!-- Línea 3 de 3 imágenes -->
            <div>
                <img src="acelerometro.jpg" alt="Acelerómetro MPU-6050" width="32%">
                <img src="presion.jpg" alt="Sensor de presión BMP180" width="32%">
                <img src="hall.jpg" alt="Sensor efecto Hall" width="32%">
            </div>
        </section>

        <!-- Sección 4: Módulos de Comunicación -->
        <section id="componentes4">
            <h2>Módulos de Comunicación</h2>

            <!-- Línea 1 de 3 imágenes -->
            <div>
                <img src="wifi-esp8266.jpg" alt="Módulo WiFi ESP8266" width="32%">
                <img src="bluetooth-hc05.jpg" alt="Módulo Bluetooth HC-05" width="32%">
                <img src="rf-433mhz.jpg" alt="Módulo RF 433MHz" width="32%">
            </div>

            <!-- Línea 2 de 3 imágenes -->
            <div>
                <img src="lora.jpg" alt="Módulo LoRa SX1278" width="32%">
                <img src="gsm-sim800l.jpg" alt="Módulo GSM SIM800L" width="32%">
                <img src="ethernet.jpg" alt="Módulo Ethernet W5500" width="32%">
            </div>

            <!-- Línea 3 de 3 imágenes -->
            <div>
                <img src="zigbee.jpg" alt="Módulo ZigBee" width="32%">
                <img src="nrf24l01.jpg" alt="Módulo NRF24L01" width="32%">
                <img src="ir.jpg" alt="Módulo Infrarrojo" width="32%">
            </div>
        </section>

        <!-- Sección 5: Herramientas y Accesorios -->
        <section id="componentes5">
            <h2>Herramientas y Accesorios</h2>

            <!-- Línea 1 de 3 imágenes -->
            <div>
                <img src="prototipado.jpg" alt="Placas de prototipado" width="32%">
                <img src="soldadura.jpg" alt="Estación de soldadura" width="32%">
                <img src="multimetro.jpg" alt="Multímetro digital" width="32%">
            </div>

            <!-- Línea 2 de 3 imágenes -->
            <div>
                <img src="fuente-alimentacion.jpg" alt="Fuente de alimentación" width="32%">
                <img src="osciloscopio.jpg" alt="Osciloscopio digital" width="32%">
                <img src="cautin.jpg" alt="Cautín profesional" width="32%">
            </div>

            <!-- Línea 3 de 3 imágenes -->
            <div>
                <img src="cables.jpg" alt="Cables y conectores" width="32%">
                <img src="brochas.jpg" alt="Brochas y limpiadores" width="32%">
                <img src="organizador.jpg" alt="Organizador de componentes" width="32%">
            </div>
        </section>
    </body>
    </html>
    ```

??? example "contacto.html"
    ```html
    <!DOCTYPE html>
    <html lang="es">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Contacto - PCBtronix</title>
    </head>
    <body>
        <!-- Barra de Navegación -->
        <nav>
            <ul>
                <li><a href="index.html">Inicio</a></li>
                <li><a href="catalogo.html">Catálogo</a></li>
                <li><a href="quienes_somos.html">Quiénes Somos</a></li>
                <li><a href="contacto.html">Contacto</a></li>
            </ul>

            <ol>
                <li><a href="#informacion">Información de Contacto</a></li>
                <li><a href="#formulario">Formulario de Contacto</a></li>
            </ol>
        </nav>

        <h1>Contáctanos</h1>

        <!-- Sección 1: Información de Contacto -->
        <section id="informacion">
            <h2>Información de Contacto</h2>
            <p>Párrafo dummy invitando a contactarnos para proyectos de diseño electrónico...</p>

            <p><strong>Dirección:</strong> Av. Tecnología 123, Parque Industrial, Ciudad</p>
            <p><strong>Teléfonos:</strong> +1 (555) 123-4567 | +1 (555) 765-4321</p>
            <p><strong>Email:</strong> info@pcbtronix.com</p>
            <p><strong>Horarios:</strong> Lunes a Viernes 8:00 - 18:00, Sábados 9:00 - 13:00</p>
        </section>

    </body>
    </html>
    ```

??? example "quienes_somos.html"
    ```html
    <!DOCTYPE html>
    <html lang="es">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Quiénes Somos - PCBtronix</title>
    </head>
    <body>
        <!-- Barra de Navegación -->
        <nav>
            <ul>
                <li><a href="index.html">Inicio</a></li>
                <li><a href="catalogo.html">Catálogo</a></li>
                <li><a href="quienes_somos.html">Quiénes Somos</a></li>
                <li><a href="contacto.html">Contacto</a></li>
            </ul>

            <ol>
                <li><a href="#historia">Nuestra Historia</a></li>
                <li><a href="#perfiles">Nuestro Equipo</a></li>
            </ol>
        </nav>

        <h1>Conoce PCBtronix</h1>

        <!-- Sección 1: Nuestra Historia -->
        <section id="historia">
            <h2>Nuestra Historia</h2>
            <p>Primer párrafo dummy sobre la fundación de PCBtronix y su visión inicial...</p>
            <p>Segundo párrafo dummy sobre el crecimiento y logros de la empresa a lo largo de los años...</p>
        </section>

        <!-- Sección 2: Perfiles del Equipo -->
        <section id="perfiles">
            <h2>Nuestro Equipo</h2>

            <!-- Perfil 1 -->
            <article>
                <h3>Nombre del Ingeniero 1</h3>
                <img src="ingeniero1.jpg" alt="Ingeniero 1" width="200">
                <p>Descripción dummy del primer ingeniero, su experiencia y especialización en diseño electrónico...</p>
            </article>

            <!-- Perfil 2 -->
            <article>
                <h3>Nombre del Ingeniero 2</h3>
                <img src="ingeniero2.jpg" alt="Ingeniero 2" width="200">
                <p>Descripción dummy del segundo ingeniero, su trayectoria y proyectos destacados...</p>
            </article>

            <!-- Perfil 3 -->
            <article>
                <h3>Nombre del Técnico</h3>
                <img src="tecnico.jpg" alt="Técnico especializado" width="200">
                <p>Descripción dummy del técnico especializado en prototipado y pruebas de circuitos...</p>
            </article>
        </section>
    </body>
    </html>
    ```

> Notas:<br>1. Las cosas que no son especificas tienes licencia creativa para agregar mas detalles.<br> 2. Ve a la [sección de recurso de imágenes](html.md#recursos-para-imagenes) para buscar imágenes de stock.

3\. Formulario de contacto simple

   1. Crea un formulario con los siguientes campos:
     1. Nombre (input tipo texto)
     2. Correo electrónico (input tipo email)
     3. Mensaje (textarea)
     4. Usa etiquetas <label> para cada campo.
     5. Agrega un botón de envío (submit).

??? example "formulario.html"
    ```html
    <!DOCTYPE html>
    <html lang="es">
    <head>
    <meta charset="UTF-8">
    <title>Formulario de contacto</title>
    </head>
    <body>

    <h1>Formulario de contacto</h1>

    <form action="#" method="post">
        <label for="nombre">Nombre:</label><br>
        <input type="text" id="nombre" name="nombre" required><br><br>

        <label for="correo">Correo electrónico:</label><br>
        <input type="email" id="correo" name="correo" required><br><br>

        <label for="mensaje">Mensaje:</label><br>
        <textarea id="mensaje" name="mensaje" rows="5" cols="30"></textarea><br><br>

        <input type="submit" value="Enviar">
    </form>

    </body>
    </html>
    ```

4\. Formulario con audio e inputs variados

   1. Crea un formulario donde el usuario pueda registrarse para escuchar un podcast.
     1. Campo de nombre y correo.
     2. Campo para elegir su género musical favorito (radio buttons).
     3. Campo para subir una foto (input tipo file).
     4. Debajo, inserta un reproductor de audio.

??? example "formulario.html"
    ```html
    <!DOCTYPE html>
    <html lang="es">
    <head>
    <meta charset="UTF-8">
    <title>Registro al Podcast</title>
    </head>
    <body>

    <h1>Registro al Podcast</h1>

    <form action="#" method="post">
        <label for="nombre">Nombre:</label><br>
        <input type="text" id="nombre" name="nombre"><br><br>

        <label for="correo">Correo electrónico:</label><br>
        <input type="email" id="correo" name="correo"><br><br>

        <p>Género musical favorito:</p>
        <input type="radio" id="rock" name="genero" value="rock">
        <label for="rock">Rock</label><br>

        <input type="radio" id="pop" name="genero" value="pop">
        <label for="pop">Pop</label><br>

        <input type="radio" id="jazz" name="genero" value="jazz">
        <label for="jazz">Jazz</label><br><br>

        <label for="foto">Sube tu foto de perfil:</label><br>
        <input type="file" id="foto" name="foto"><br><br>

        <input type="submit" value="Registrarse">
    </form>

    <h2>Escucha un fragmento de nuestro podcast:</h2>
    <audio controls>
        <source src="podcast.mp3" type="audio/mpeg">
        Tu navegador no soporta el elemento de audio.
    </audio>

    </body>
    </html>
    ```

## CSS

1. Título con fuentes personalizadas y transformación de texto
     1. Crea un encabezado `<h1>` con un subtítulo `<p>`.
     1. Usa `@font-face` para cargar una fuente personalizada (o un archivo local).
     1. Aplica `text-transform`, `letter-spacing`, `font-family`, `font-weight` y `text-align`.

??? example "formulario.html"
    ```html
    <!DOCTYPE html>
    <html lang="es">
    <head>
    <meta charset="UTF-8">
    <title>Ejercicio 1 - Fuentes y Transformaciones</title>
    <style>
    @font-face {
    font-family: 'MiFuente';
    src: url('MiFuente.woff2') format('woff2');
    }

    h1 {
    font-family: 'MiFuente', Arial, sans-serif;
    font-size: 2.5em;
    font-weight: 700;
    text-transform: uppercase;
    text-align: center;
    letter-spacing: 5px;
    color: #2c3e50;
    }

    p {
    text-align: center;
    font-style: italic;
    color: #7f8c8d;
    }
    </style>
    </head>
    <body>

    <h1>Diseño de Texto en CSS</h1>
    <p>Usando fuentes personalizadas y transformaciones de texto.</p>

    </body>
    </html>
    ```

2\. Texto con sombra, decoración y espaciado

   1. Crea un párrafo destacado.
     1. Aplica color, text-shadow, text-decoration, word-spacing, y line-height.
     2. Experimenta con diferentes valores de text-shadow para crear profundidad.

??? example "formulario.html"
    ```html
    <!DOCTYPE html>
    <html lang="es">
    <head>
    <meta charset="UTF-8">
    <title>Ejercicio 2 - Sombras y Espaciado</title>
    <style>
    p {
    font-family: 'Georgia', serif;
    font-size: 20px;
    color: #34495e;
    line-height: 1.8;
    word-spacing: 10px;
    text-decoration: underline dotted #2980b9;
    text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
    }
    </style>
    </head>
    <body>

    <p>El texto con sombras y espaciado crea una sensación visual más atractiva y profesional.</p>

    </body>
    </html>
    ```

3\. Diferentes estilos y pesos de fuente

1. Crea tres párrafos con distintas combinaciones de:
    1. `font-family`
    1. `font-size`
    1. `font-style`
    1. `font-weight`
    1. `color`
    1. `text-align`
2. Usa distintas familias (`serif`, `sans-serif`, `monospace`).

??? example "formulario.html"
    ```html
    <!DOCTYPE html>
    <html lang="es">
    <head>
    <meta charset="UTF-8">
    <title>Ejercicio 4 - Estilos Tipográficos</title>
    <style>
    .serif {
    font-family: 'Times New Roman', serif;
    font-size: 22px;
    font-weight: bold;
    color: #8e44ad;
    text-align: left;
    }

    .sans {
    font-family: 'Arial', sans-serif;
    font-size: 18px;
    font-style: italic;
    color: #27ae60;
    text-align: center;
    }

    .mono {
    font-family: 'Courier New', monospace;
    font-size: 16px;
    color: #c0392b;
    font-weight: 300;
    text-align: right;
    }
    </style>
    </head>
    <body>

    <p class="serif">Texto con fuente Serif: elegante y tradicional.</p>
    <p class="sans">Texto con fuente Sans-serif: moderna y limpia.</p>
    <p class="mono">Texto con fuente Monospace: ideal para código o terminales.</p>

    </body>
    </html>
    ```

### Position

??? example "Guía de referencia"
    ![position](img/widgets/position.png)

1. Cómo `position relative` no saca al elemento del flujo, pero te permite moverlo respecto a su posición normal.

Instrucciones:

- Crea un `<div>` de 150×150 px con color de fondo (cualquiera).
  - Asigna position: relative.
  - Aplica propiedades de desplazamiento como:
    - `top: 20px;`
    - `left: 30px;`

??? example "index.html"
    ```html
    <div class="caja">Caja</div>
    ```


    ??? example "css.css"
        ```css
        .caja {
            width: 150px;
            height: 150px;
            background: coral;
            position: relative;
            top: 20px;
            left: 30px;
        }
        ```

2\. Usar `position: absolute` dentro de un contenedor. Un elemento con `position absolute` se posiciona respecto a su contenedor más cercano con `position: relative`.

Instrucciones:

- Crea un `<div>` grande llamado .contenedor.
- Dale width, height y un fondo para verlo (por ejemplo lightgray).
- Dentro del contenedor, crea otro <div> llamado .absoluto.
- Al contenedor aplícale position: relative.
- Al `div` interno aplícale:
    - `position: absolute;`
    - `bottom: 10px;`
    - `right: 10px;`
- Observa que el elemento hijo:
    - Se pega a la esquina inferior derecha del contenedor.
    - No se posiciona respecto al body.

??? example

    ??? example "index.html"
        ```html
        <div class="contenedor">
          <div class="absoluto">Soy absoluto</div>
        </div>

        ```


    ??? example "css.css"
        ```css
        .contenedor {
          width: 300px;
          height: 200px;
          background: lightgray;
          position: relative;
        }

        .absoluto {
          position: absolute;
          bottom: 10px;
          right: 10px;
          background: tomato;
          padding: 10px;
        }
        ```

3 \. Crear una barra fija con `position: fixed`. Los elementos con `position: fixed` se fijan a la ventana, no al documento.

- Crea un `<header>` con clase `.barra`.
- Rellénalo con cualquier texto para simular un menú.
- Aplica `position: fixed`;.
- Posiciónalo con:
    - top: 0;
    - left: 0;
- Dale `width: 100%` para que ocupe todo el ancho.
- Agrega bastante texto al documento para poder hacer scroll.
- Observa que:
    - El header **siempre permanece visible**, aunque te desplaces.


??? example

    ??? example "index.html"
        ```html
        <div class="contenedor">
          <div class="absoluto">Soy absoluto</div>
        </div>
        ```


    ??? example "css.css"
        ```css
        .contenedor {
            width: 300px;
            height: 200px;
            background: lightgray;
            position: relative;
            }

        .absoluto {
            position: absolute;
            bottom: 10px;
            right: 10px;
            background: tomato;
            padding: 10px;
        }
        ```

## Widgets

### Crear estilos de botones

Realizar todos los estilos de botones que se muestran en la imagen. Siempre debes usar `clases`. Puedes elegir el color que desees de base, lo que se muestra es una referencia.

![botones](img/widgets/botones.png)

> Notas: <br>Recurso: [iconos de bootstrap](https://icons.getbootstrap.com) <br>
> Recurso: [iconos de google](https://fonts.google.com/icons)

### Crear estilos de Cards

Realizar todos los estilos de cards que se muestran en la imagen. Siempre debes usar `clases`. Para los gradientes puedes usar la herramienta que prefieras o hay recursos que te comparto.

![cards](img/widgets/cards.png)

> Notas: Referncia: [Cards de bootstrap](https://getbootstrap.com/docs/5.0/components/card/)
> <br>Recurso: Generador de gradientes: [Gradient Generator](https://cssgradient.io/)
> <br>Recurso: Generador de gradientes: [Gradient Generator](https://uigradients.com/)

## Sitio webs de practica

Reproducir los siguientes sitios

??? note "Mock-up"
    ![mockup](https://raw.githubusercontent.com/jalmx/html-class/refs/heads/master/mockup/mockup_.png)

??? note "CV"
    ![cv](img/sites/cv_template.jpg)

??? note "Sitio de los tigres"
    ![https://raw.githubusercontent.com/jalmx89/Dummy-templates/master/view/tigerZooWeb.png](https://raw.githubusercontent.com/jalmx89/Dummy-templates/master/view/tigerZooWeb.png)

??? note "Consultoría"
    ![consultoria](img/sites/site2.png)
