# Proyectos

## Project 1 - Tienda electrónica

### Vista del sitio web

![Project 1](project_template.png)

### Arquitectura

```bash
├── fonts
│   ├── bootstrap-icons.woff
│   └── bootstrap-icons.woff2
├── imgs
│   ├── banner.png
│   ├── logo_org.svg
│   ├── logo.png
│   └── logo.svg
├── index.html
└── style
    ├── bootstrap-icons.css
    ├── bootstrap-icons.min.css
    └── css.css
```

Descarga proyecto: [project1.zip](./project1.zip)

### Código

??? example "index.html"
    ```html
    <!DOCTYPE html>
    <html lang="en">

    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>ElectroDesign</title>
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100..900;1,100..900&display=swap"
            rel="stylesheet">
        <link rel="stylesheet" href="style/bootstrap-icons.css">
        <link rel="stylesheet" href="style/css.css">
    </head>

    <body>

        <nav class="nav">
            <div class="logo">
                <img src="imgs/logo.png" class="logo__img" alt="logo">
                <h3>ElectroDesign</h3>
            </div>
            <ul class="menu">
                <li class="menu__item"><a class="menu__link" href="#">Servicios</a></li>
                <li class="menu__item"><a class="menu__link" href="#">Clientes</a></li>
                <li class="menu__item"><a class="menu__link" href="#">Contactos</a></li>
                <li class="menu__item"><a class="menu__link button" href="#">Cotizar proyecto</a></li>
            </ul>
        </nav>
        <header class="header">
            <div class="header__title">Soluciones Electrónicas Integrales a tu Medida</div>
            <p class="header__text">Ofrecemos diseño de vanguardia, asesoramiento experto y venta de componentes de alta
                calidad para llevar tus proyectos al siguiente nivel.</p>
            <div class="">
                <a class="button" href="#">Ver servicios</a>
            </div>
        </header>
        <main>
            <section class="services">
                <div>
                    <h2 class="services__title">Nuestros Servicios</h2>
                    <p class="services__description">Cubrimos todo el ciclo de la vida de tu producto, desde la concepción
                        hasta la producción.</p>
                    <div class="service__text"></div>
                </div>
                <section class="cards">
                    <article class="card">
                        <i class="bi bi-cpu"></i>
                        <header class="card__title">
                            Diseño Electrónico</header>
                        <p class="card__text">Creamos circuitos innovadores y eficientes para tus necesidades específicas.
                        </p>
                    </article>
                    <article class="card">
                        <i class="bi bi-grid-1x2-fill"></i>
                        <header class="card__title">Diseño de PCB</header>
                        <p class="card__text">Diseñamos placas de circuito impreso optimizadas para rendimiento y
                            fabricación.
                        </p>
                    </article>
                    <article class="card">
                        <i class="bi bi-person-workspace"></i>
                        <header class="card__title">Asesoramiento Técnico</header>
                        <p class="card__text">Te guiamos con nuestra experiencia para asegurar el éxito de tu proyecto.</p>
                    </article>
                    <article class="card">
                        <i class="bi bi-robot"></i>
                        <header class="card__title">Venta de Componentes</header>
                        <p class="card__text">Accede a un amplio catálogo de componentes electrónicos de alta calidad.</p>
                    </article>
                </section>

            </section>
            <!--
            <section class="client">
                <h2 class="client__title">Lo que dicen nuestros clientes</h2>
                <section class="client__cards">
                    <article class="card2">
                        <img src="" alt="">
                        <p class="card2__info">"El equipo de ElectroDesign transformó nuestra idea en un producto funcional
                            en tiempo récord. Su asesoramiento fue clave para el éxito."</p>
                        <footer><span class="card2__name">Juan Pérez</span><span class="card2__profile">CEO,
                                InnovaTech</span></footer>
                    </article>
                    <article class="card2">
                        <img src="" alt="">
                        <p class="card2__info">"La calidad de los componentes y la rapidez en la entrega son insuperables.
                            Son nuestro proveedor de confianza."</p>
                        <footer><span class="card2__name">Ana García</span>Directora de I+D, Soluciones Futuras<span
                                class="card2__profile"></span></footer>
                    </article>
                    <article class="card2">
                        <img src="" alt="">
                        <p class="card2__info">"Desde el diseño del PCB hasta la selección de componentes, su equipo
                            demostró un profesionalismo y conocimiento excepcionales."</p>
                        <footer><span class="card2__name">Carlos Rodríguez</span><span class="card2__profile">Ingeniero
                                Jefe, Gadget Co.</span></footer>
                    </article>
                </section>
            </section> -->

            <section class="contact">
                <h2 class="contact__title">Hablemos de tu proyecto</h2>
                <section class="contact__container">
                    <div class="form">
                        <h2 class="contact__title">Enviar mensaje</h2>
                        <form class="contact__form">
                            <!-- <label for="name">Nombre:</label> -->
                            <input class="form__input" type="text" id="name" name="name" placeholder="Nombre" required>
                            <!-- <label for="email">Correo:</label> -->
                            <input class="form__input" type="email" id="email" name="email" placeholder="Email" required>
                            <input class="form__input" type="text" id="name" name="name" placeholder="Asunto" required>
                            <!-- <label for="message">Tu mensaje</label> -->

                            <textarea class="form__input textarea" id="message" name="message" placeholder="Tu mensaje"
                                rows="8" required></textarea>

                            <input type="submit" value="Enviar Mensaje" class="button">
                        </form>
                    </div>
                    <div class="info">
                        <h2 class="contact__title">Información de Contacto</h2>
                        <div class="info__container">
                            <i class="bi bi-pin-map-fill"></i>
                            <div class="info__text"></i> Av. de la Tecnología 123, Parque Tecnológico, 28001 Coatzacoalcos, Veracruz, Mexico</div>
                        </div>

                        <div class="info__container">
                            <i class="bi bi-telephone-fill"></i>
                            <div class="info__text"> +52 921 345 678</div>
                        </div>

                        <div class="info__container">
                            <i class="bi bi-envelope-fill"></i>
                            <div class="info__text"> contacto@electrodesign.com</div>
                        </div>

                        <iframe
                            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1386.8451815640947!2d-94.42553197362753!3d18.139468937920586!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x85e982588fffffff%3A0x12a620cf1087c4de!2sCBTIS%20n%C2%B085!5e0!3m2!1sen!2smx!4v1762985460409!5m2!1sen!2smx"

                            class="map" loading="lazy"
                            referrerpolicy="no-referrer-when-downgrade"></iframe>
                    </div>
                </section>

            </section>
        </main>
        <footer class="footer">
            <section class="footer__section">
                <h2 class="footer__title">Navegación</h2>
                <ul class="footer__list">
                    <li class="footer__item"><a class="footer__link" href="#">Servicios</a></li>
                    <li class="footer__item"><a class="footer__link" href="#">Clientes</a></li>
                    <li class="footer__item"><a class="footer__link" href="#">Contacto</a></li>
                </ul>
            </section>
            <section class="footer__section">
                <h2 class="footer__title">Legal</h2>
                <ul class="footer__list">
                    <li class="footer__item"><a class="footer__link" href="#">Política de privacidad</a></li>
                    <li class="footer__item"><a class="footer__link" href="#">Términos y condiciones</a></li>
                </ul>
            </section>
            <section class="footer__section">
                <h2 class="footer__title">Síguenos</h2>
                <ul class="footer__list footer__networks">
                    <li class="footer__item"><a href="#"><i class="footer__icon bi bi-facebook"></i></a></li>
                    <li class="footer__item"><a href="#"><i class="footer__icon bi bi-twitter"></i></a></li>
                    <li class="footer__item"><a href="#"><i class="footer__icon bi bi-youtube"></i></a></li>
                </ul>
            </section>
        </footer>
        <div class="footer__copy">
            <h3>&#169; 2024 ElectroDesign. Todos los derechos reservados.</h3>
        </div>
    </body>

    </html>
    ```

??? example "style/css.css"
    ```css
    :root,
    html,
    body,
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-weight: 400;

        font-family: "Roboto", sans-serif;
        font-optical-sizing: auto;
        font-variation-settings: "wdth" 100;

        --background: #f6f7f8;
        --primary: #137fec;
        --font: #4a5565;
    }

    body {
        background-color: var(--background);
        max-width: 1200px;
        margin: auto;

    }

    .nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        padding: 1rem 2rem;
        font-size: 0.9rem;
        margin-bottom: 1rem;
        position: relative;
    }

    nav::after {
        content: "";
        position: absolute;
        bottom: 0;
        left: 50%;
        min-width: 100%;
        max-width: 1200px;
        height: 1px;
        background-color: var(--font);
        opacity: 0.2;
        transform: translateX(-50%);
        box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.5);
    }

    .logo {
        display: flex;
        height: 3rem;
        justify-content: center;
        align-items: center;

    }

    .logo__img {
        width: 100%;
        height: 100%;
        display: flex;
        padding: 4px;
        margin-right: 1rem;
    }

    .menu {
        list-style: none;
        display: flex;
        align-items: center;
    }

    .menu__item {
        margin-left: 1rem;
    }

    .menu__link {
        color: var(--font);
        text-decoration: none;
        text-transform: uppercase;
        padding: 0.5rem .5rem;
    }


    .button {
        color: var(--background);
        background-color: var(--primary);
        padding: .6rem 1.5rem;
        border-radius: 5px;
        font-weight: bold;
        text-decoration: none;
        border: none;
    }

    .header {
        height: 400px;
        position: relative;
        margin-bottom: 3rem;

    }

    .header::before {
        content: "";
        background-image: url('../imgs/banner.png');
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        width: 100%;
        height: 100%;
        position: absolute;
        filter: blur(2px);
        z-index: -1;

    }

    .header::after {
        content: "";
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        background-color: rgba(0, 0, 0, 0.4);
        filter: blur(2px);
        z-index: -1;
    }

    .header__title {
        font-size: 3rem;
        font-weight: bold;
        letter-spacing: 1px;
        color: var(--background);
        margin: auto;
        padding: 3rem 1rem;

    }

    .header__text {
        color: var(--background);
        font-size: 1.5rem;
        padding: 1rem 1rem;
        padding-bottom: 2rem;
    }

    .header .button {
        margin-left: 1rem;
    }

    .services {
        padding: 2rem 1rem;
    }

    .services__title {
        font-weight: 600;
        font-size: 2rem;
    }

    .service__text {
        font-weight: 100;
    }

    .services__description {
        padding: 2rem 0;
        font-size: 1.2rem;
        color: var(--font);
    }

    .cards {
        display: flex;
        justify-content: space-between;
        flex: 1;
        flex-wrap: wrap;
        gap: 2rem;
        align-content: center;
    }

    .card {
        background-color: white;
        border-radius: 10px;
        box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
        padding: 2rem;
        min-width: 320px;
        width: 350px;
        display: flex;
        flex-direction: column;
    }

    .bi {
        color: var(--primary);
        font-size: 1.6rem;
        font-weight: bold;
        margin-bottom: 1rem;
    }

    .card__title {
        font-size: 1.3rem;
        font-weight: 600;
        margin-bottom: .5rem;
    }

    .card__text {
        color: var(--font);
        font-size: .9rem;
        line-height: 1.5;
    }

    .contact {
        overflow: hidden;
        padding: 2rem;
    }

    .contact__container {
        background-color: white;
        display: flex;
        justify-content: space-between;
        padding: 2rem;
        border-radius: 8px;
    }

    .contact__title {
        font-weight: bold;
        text-align: center;
        font-size: 2rem;
        padding-bottom: 2rem;
    }

    .form,
    .info {
        width: 48%;
        display: flex;
        flex-direction: column;
    }

    .contact__form {
        display: flex;
        flex-direction: column;
    }

    .form__input {
        padding: .5rem;
        margin-bottom: .5rem;
        border-radius: 5px;
        background-color: var(--background);
        border: 1px solid var(--primary);
        font-size: 16px;
    }

    .info__text {
        font-size: 1rem;
        color: var(--font);
        letter-spacing: 0.5px;
    }

    .info__container {
        display: flex;
        margin-bottom: .5rem;
    }

    .info__container .bi {
        font-size: 1rem;
        margin-right: .5rem;
    }

    .map {
        border: 0;
        width: 100%;
        height: 200px;
        border-radius: 10px;
    }

    .footer {
        display: flex;
        justify-content: space-around;
        padding: 1rem;
    }

    .footer__section {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
    }

    .footer__list {
        flex-grow: 2;
        list-style: none;
        display: flex;
        flex-direction: column;

    }

    .footer__title {
        font-weight: 500;
        padding-bottom: 1rem;
    }
    .footer__item {
        padding-bottom: 1rem;
    }

    .footer__link {
        color: var(--font);
        text-decoration: none;
    }

    .footer__networks {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }
    .footer__copy {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 1rem;
        color: var(--font);
        position: relative;
    }

    .footer__copy::after {
        content: "";
        position: absolute;
        top: 0;
        left: 50%;
        min-width: 100%;
        max-width: 1200px;
        height: 1px;
        background-color: var(--font);
        opacity: 0.2;
        transform: translateX(-50%);
        box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.5);
    }
    ```

