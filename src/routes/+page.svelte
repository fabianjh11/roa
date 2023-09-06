<script>
    import { onMount } from 'svelte';
    import Materias from './materias.svelte';
    import Slider from './slider.svelte';

    onMount(() => {
        document.body.addEventListener('click', handleBodyClick);
        return () => {
            document.body.removeEventListener('click', handleBodyClick);
        };
    });

    let materiaSeleccionada = "";
    let id = "";
    let display = false;

    function handleClick(event) {
        id = event.currentTarget.getAttribute('id');
        if(id == "menu") {
            display = !display;
            return;
        }
        display = false;
        materiaSeleccionada = id;
        event.stopPropagation();
    }

    function handleBodyClick() {
        materiaSeleccionada = "";
    }



</script>
    
<main>
    <div class="navbar">
        <div class="items">
            <h4 class="t-navbar">ROA</h4>
            
            <!--Menú desplegable-->
            <!-- svelte-ignore a11y-click-events-have-key-events -->
            <!-- svelte-ignore a11y-no-static-element-interactions -->
            <div id="menu" class="menu" on:click={handleClick}>
                <button  class={ display? 'b-close':'b-menu'}>
                    <div class="bar"></div>
                    <div class="bar"></div>
                    <div class="bar"></div>
                </button>
                {#if display}
                    <div class="menu-options">
                        <h5><a href="#inicio">Inicio</a></h5>
                        <h5><a href="#nosotros">Nosotros</a></h5>
                        <h5><a href="#servicios">Servicios</a></h5>
                        <h5><a href="#contacto">Contacto</a></h5>
                        <h5><a href="#ubicacion">Ubicación</a></h5>
                    </div>
                {/if}
            </div>

            <!--Menú general-->
            <div class="menu-amplio">
                <h5><a href="#inicio">Inicio</a></h5>
                <h5><a href="#nosotros">Nosotros</a></h5>
                <h5><a href="#servicios">Servicios</a></h5>
                <h5><a href="#contacto">Contacto</a></h5>
                <h5><a href="#ubicacion">Ubicación</a></h5>
            </div>
        </div>
    </div>

    <div class="space" id="inicio"></div>
    <div class="space"></div>
    
    <div class="main">
        <div class="titulos">
            <h1 class="titulo">ROA</h1>
            <h3>Corporativo Jurídico</h3>
            <p>No basta con decir lo bueno que eres, sino, demostrarlo a la hora de enfrentar
                el problema, ahí es donde todo vale.
            </p>
        </div>
        <div class="slider">
            <Slider></Slider>
        </div>
    </div>

    <div class="space"></div>
    <div class="space-color" id="nosotros"></div>
    <div class="space"></div>

    <div class="nosotros">
        <h4>Nosotros</h4>
        <p>
            Bienvenido a ROA Corporativo Jurídico, somos un equipo de
            Abogados con experiencia en cientos de litigios de diversas
            órdenes y materias, dispuestos a solucionar todo tipo de
            controversias que se susciten; nuestra inteligencia, responsabilidad,
            capacidad de solución de problemas y transparencia es el punto focal
            de este despacho.
        </p> 
    </div>

    <div class="space"></div>
    <div class="space-color"  id="servicios"></div>
    <div class="space"></div>

    <div class="mid">
        <h4 class="frase">¿Cuál es tu problema?</h4>
    </div>

    <br>

    <div class="middle">
        <div class="materias">
            <button id="m1" on:click={handleClick}>Penal</button>
            <button id="m2" on:click={handleClick}>Familiar</button>
            <button id="m3" on:click={handleClick}>Civil</button>
            <button id="m4" on:click={handleClick}>Mercantil</button>
            <button id="m5" on:click={handleClick}>Administrativo</button>
            <button id="m6" on:click={handleClick}>Laboral</button>
        </div>
    </div>
    <div class="space"></div>

    <Materias materia={materiaSeleccionada}></Materias>

    <div class="space"></div>
    <div class="space-color"  id="contacto"></div>
    <div class="space"></div>

    <div class="contacto">
        <h4>Contacto</h4>

        <br>
        <p>Contacta a alguno de nuestros abogados</p>
        <br>

        <div class="logos">
            <a class="logo-Whatsapp" id="NumeroDeKevin" href="https://api.whatsapp.com/send?phone=3331727807" target="_blank">
                <svg xmlns="http://www.w3.org/2000/svg" width="8vw" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                    <path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/>
                </svg>
            </a>
    
            <a class="logo-Whatsapp" id="NumeroDeSocia" href="https://api.whatsapp.com/send?phone=3861033922" target="_blank">
                <svg xmlns="http://www.w3.org/2000/svg" width="8vw" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                    <path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/>
                </svg>
            </a>
        </div>
        
        <div class="contactos">
            <h3>Lic. Kevin Ramos</h3>
            <h3>Lic. Guadalupe Ayón</h3>
        </div>

        <div class="space"></div>
        <div class="logos">
            <a class="logo-Whatsapp" id="NumeroDeSocia" href="https://api.whatsapp.com/send?phone=5510701139" target="_blank">
                <svg xmlns="http://www.w3.org/2000/svg" width="8vw" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                    <path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/>
                </svg>
            </a>
        </div>
        <div class="contactos">
            <h3>Lic. Mauricio Aguilar Laureano</h3>
        </div>

    </div>

    <div class="space"></div>
    <div class="space-color" id="ubicacion"></div>
    <div class="space"></div>

    <div class="ubicacion">
        <h4>Visítanos aquí</h4>
        <br>
        <p>5 de Mayo 257, Santa Anita, Tlaquepaque, Jalisco.</p>
        <br>
        <div class="map-container">
            <div class="aerialview">
                <!-- svelte-ignore a11y-missing-attribute -->
                <iframe class="" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1867.930773342425!2d-103.44576596920798!3d20.552845059565616!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x842f535a00b7a9ff%3A0x7754616390215256!2s5%20de%20Mayo%20257%2C%2045600%20Santa%20Anita%2C%20Jal.!5e0!3m2!1ses-419!2smx!4v1693101799617!5m2!1ses-419!2smx" 
                        allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade">
                </iframe>
            </div>
        </div>
    </div>

    <div class="space"></div>

    <footer>
        <p>©2023 ROA - Corporativo Jurídico</p>
        <br>
        <p>Todos los derechos reservados</p>
    </footer>

</main>

<style>
    :root {
        --dark: #182322;
        --light: #F5F6EB;
        --main: #044a53;
        --contrast: #CDE49A;
        --main2: #6cb2b6;
    }
    main{
        background-color: var(--light);
        font-family: 'Montserrat', sans-serif;
        color: var(--dark);
    }

    .navbar{
        background: linear-gradient(to right, var(--dark), var(--main));
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        padding: 10px;
        min-height: 5vh;
        display: flex;
        align-items: center;
        justify-content: space-between;
        z-index: 5;
    }

    .items{
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
    }

    .t-navbar{
        padding-left: 1%;
        font-size: 3vh;
        color: var(--light);
        cursor: pointer;
    }

    .b-menu, .b-close {
        border: 0;
        background-color: transparent;
        display: flex;
        flex-direction: column;
        min-width: 2rem;
        gap: 0.51rem;
    }
    .b-menu .bar, .b-close .bar {
        background: var(--light);
        height: 2.5px;
        width: 95%;
        border-radius: 5px;
        transform-origin: left;
        transition: all 0.2s ease-in-out;
    }

    .b-close .bar:first-child {
        transform: rotate(45deg);
    }
    .b-close .bar:nth-child(2) {
        opacity: 0;
    }
    .b-close .bar:last-child {
        transform: rotate(-45deg);
    }

    .menu-amplio {
        display: none;
    }

    .menu {
        position: relative;
        display: inline-block;
        margin-right: 30px;
    }

    .menu-options {
        position: absolute;
        padding-top: 15px;
        min-width: 19vw;
        box-shadow: 0px 10px 16px 0px rgba(0,0,0,0.3);
        right: -3px;
        opacity: 0.85;
        text-align: center;
    }

    .menu-options h5 {
        background-color: var(--main2);
    }
    .menu-options h5 a {
        color: var(--light);
        padding: 12px 16px;
        text-decoration: none;
        display: block;
    }

    .menu-options h5 a:hover {
        background-color: var(--light);
        color: var(--dark);
        cursor: pointer;
        box-shadow: 0px 0px 10px 5px var(--main);
    }

    .space {
        min-height: 5vh;
        padding: 10px;
    }
    .space-color {
        min-height: 5vh;
        padding: 10px;
        background-color: var(--main);
    }

    .main{
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        z-index: 0;
    }

    .slider{
        width: 100%;
    }

    .titulos{
        position: absolute;
        z-index: 1;
        font-size: 6vw;
        text-align: center;
        width: 90%;
        font-family: 'Raleway', sans-serif;
    }
    .titulos h1 {
        color: var(--light);
        text-shadow: 1px 2px 5px var(--main);
    }
    .titulos h3 {
        color: var(--main);
        text-shadow: 1px 1px 5px var(--light);
        font-weight: bold;
    }
    .titulos p {
        margin-top: 2vh;
        font-size: 2vw;
        color: var(--light);
        text-shadow: 1px 1px 1px var(--dark);
    }

    .nosotros {
        justify-content: center;
        align-items: center;
        padding: 50px;
    }
    .nosotros h4 {
        color: var(--main2);
        font-size: 4vw;
        text-align: center;
        padding: 10px;
        font-family: 'Raleway';
    }

    .nosotros p {
        text-align:justify;
        padding: 20px 100px;
        font-size: 2vw;
    }

    .mid {
        min-height: 7vh;
        padding: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .frase {
        font-size: 4vw;
        text-align: center;
        color: var(--main2);
        padding: 10px;
        font-family:'Raleway';
    }

    .middle {
        display: flex;
        justify-content: center;
    }
    .materias {
        max-width: 80%;
        display: grid;
        justify-content: space-between;
        grid-template-columns: repeat(2, 5fr);
    }
    .materias button {
        padding: 10px;
        margin: 5px;
        border: none;
        border-bottom: solid 3px var(--dark);
        background-color: var(--light);
        border-radius: 1px;
        cursor: pointer;
        font-size: 3vw;
        color: var(--dark);
        font-family: 'Montserrat', sans-serif;
    }

    .materias button:hover {
        color: var(--main);
        border-bottom: none;
        background: linear-gradient(to top, #c7ebed, var(--light));
        border-radius: 10px;
        box-shadow: 0px 0px 10px 1px var(--main2);
    }

    .contacto {
        justify-content: center;
        align-items: center;
        padding: 50px;
    }
    .contacto h4 {
        color: var(--main2);
        font-size: 4vw;
        text-align: center;
        padding: 10px;
        font-family: 'Raleway';
    }
    .contacto p {
        font-size: 3vw;
        text-align: center;
    }

    .logos {
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 10px;
    }
    .logo-Whatsapp{
        fill: var(--main2);
    }
    .logo-Whatsapp:hover{
        fill: var(--main);
    }

    .contactos {
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 10px;
    }
    .contactos h3 {
        font-size: 3vw;
        font-family: 'Raleway';
    }

    .map-container{
        overflow: hidden;
        position: relative;
        padding-bottom: 50%;
    }

    .ubicacion {
        justify-content: center;
        align-items: center;
        padding: 50px;
    }
    .ubicacion h4 {
        color: var(--main2);
        font-size: 4vw;
        text-align: center;
        padding: 10px;
        font-family: 'Raleway';
    }
    .ubicacion p {
        font-size: 3vw;
        text-align: center;
    }

    iframe{
        height: 100%;
        width: 100%;
        position: absolute;
    }

    footer {
        background-color: var(--main);
        color: var(--light);
        padding: 200px 0px;
        width: 100%;
    }
    footer p {
        text-align: center;
        font-size: 1.5vw;
    }

    @media (max-width: 900px) {
        .slider {
            width: 100%;
        }
        .nosotros p {
            font-size: 4vw;
            padding: 20px;
        }
        .nosotros {
            padding: 10px;
        }
        .nosotros h4 {
            font-size: 6vw;
        }
        .space {
            min-height: 3vh;
        }
        .space-color {
            min-height: 3vh;
        }
        .contacto {
            padding: 10px;
        }
        .contacto h4 {
            font-size: 6vw;
        }
        .contacto p {
            font-size: 4vw;
            padding: 10px;
        }
        .frase {
            font-size: 6vw;
        }
        .ubicacion {
            padding: 10px;
        }
        .ubicacion h4 {
            font-size: 6vw;
        }
        .ubicacion p {
            font-size: 4vw;
            padding: 10px;
        }
        footer p{
            font-size: 3vw;
        }
    }

    @media screen and (max-width: 300px) {
        .frase {
            font-size: 5vw;
        }
        .materias button {
            font-size: 4vw;
        }
    }

    @media screen and (min-width: 750px) {
        .menu {
            display: none;
        }
        .menu-amplio {
            display: flex;
            padding-right: 50px;
        }
        .menu-amplio *{
            padding: 10px;
        }
        .menu-amplio h5 a{
            text-decoration: none;
            color: #D3D4C9;
        }

        .menu-amplio h5 a:hover {
            color: #FFF;
        }

        .materias{
            grid-template-columns: repeat(3, 1fr);
        }
    }
</style>
