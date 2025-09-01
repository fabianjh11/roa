<script>
    import Navabar from '../lib/components/navabar.svelte';
    import MateriasSlider from '../lib/components/materiasSlider.svelte';
    import Slider from '../lib/components/slider.svelte';
    import Contacto from '../lib/components/contacto.svelte';
    import Ubicacion from '../lib/components/ubicacion.svelte';
    import Footer from '../lib/components/footer.svelte';
  import BotonWa from '../lib/components/botonWA.svelte';
  import Comentarios from '../lib/components/comentarios.svelte';
</script>
    
<main>
    <Navabar/>

    <div class="space" id="inicio"></div>
    
    <div class="main">
        <div class="titulos">
            <h1>Abogados expertos en Civil, Mercantil, Familiar y Penal</h1>
            <p>Resolvemos tu caso con experiencia y resultados comprobados.</p>

            <div class="cta-botones">
                <a href="tel:+3331727807" class="btn-llamar">
                    <svg class="telefono-logo" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 640">
                        <!--!Font Awesome Free v7.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.-->
                        <path d="M224.2 89C216.3 70.1 195.7 60.1 176.1 65.4L170.6 66.9C106 84.5 50.8 147.1 66.9 223.3C104 398.3 241.7 536 416.7 573.1C493 589.3 555.5 534 573.1 469.4L574.6 463.9C580 444.2 569.9 423.6 551.1 415.8L453.8 375.3C437.3 368.4 418.2 373.2 406.8 387.1L368.2 434.3C297.9 399.4 241.3 341 208.8 269.3L253 233.3C266.9 222 271.6 202.9 264.8 186.3L224.2 89z"/>
                    </svg>
                    Llamar ahora
                </a>
                <a href="https://api.whatsapp.com/send?phone=3331727807&text=Hola%2C%20vengo%20del%20sitio%20web%20ROA%20CORPORATIVO%20JURIDICO%2C%20quisiera%20brindar%20información%20sobre%20mi%20asunto%2E" target="_blank" class="btn-whatsapp">
                    <svg class="whatsapp-logo" xmlns="http://www.w3.org/2000/svg" width="8vw" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                        <path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/>
                    </svg>
                    WhatsApp 24/7
                </a>
            </div>
        </div>
        <div class="slider">
            <Slider/>
        </div>
    </div>

    <div class="middle">
        <div class="mid">
            <h4 class="sub-titulo sub-titulo-1">Servicios:</h4>
            <h5 class="sub-titulo sub-titulo-2">Derecho Especialidad</h5>
        </div>
        <MateriasSlider />
    </div>

    <Comentarios />

    <Contacto />

    <Ubicacion />

    <BotonWa />

    <Footer />
</main>

<style>
    :root {
        --dark: #182322;
        --light: #F5F6EB;
        --main: #044a53;
        --contrast: #CDE49A;
        --main2: #6cb2b6;
        --main3: #96cacd;
    }
    main{
        background-color: var(--light);
        font-family: 'Montserrat', sans-serif;
        color: var(--dark);
    }

    .space {
        min-height: 5vh;
        padding: 10px;
    }

    .main{
        position: relative;
        display: flex;
        align-items: flex-end;
        justify-content: center;
        z-index: 0;
    }

    .slider{
        width: 100%;
        max-height: 92vh;
    }

    .titulos{
        position: absolute;
        z-index: 1;
        font-size: 5vw;
        text-align: center;
        width: 100%;
        font-family: 'Raleway', sans-serif;
        padding-bottom: 3%;
    }
    .titulos h1 {
        color: var(--light);
        text-shadow: 1px 2px 5px var(--main);
        font-size: 1em;
    }
    .titulos p {
        margin-top: 2vh;
        font-size: 2.5vw;
        color: var(--light);
        text-shadow: 1px 1px 1px var(--dark);
    }
    .cta-botones {
        margin-top: 2vh;
        display: flex;
        justify-content: space-evenly;
        flex-wrap: wrap;
        font-family: 'Montserrat', sans-serif;
    }
    .cta-botones a {
        padding: 8px 18px;
        font-size: 0.8rem;
        font-weight: bold;
        border-radius: 6px;
        text-decoration: none;
        transition: all 0.3s ease;
        box-shadow: 1px 1px 8px rgba(0,0,0,0.8);
    }
    .btn-llamar {
        display: flex;
        gap: 8px;
        background-color: var(--light);
        color: var(--main);
        justify-content: center;
        align-items: center;
    }
    .telefono-logo {
        fill: var(--main);
        width: 16px;
    }
    .btn-llamar:hover {
        background-color: var(--main2);
    }
    .btn-whatsapp {
        background-color: var(--main);
        color: var(--light);
        display: flex;
        gap: 8px;
        justify-content: center;
        align-items: center;
    }
    .whatsapp-logo {
        fill: var(--light);
        width: 16px;
    }
    .btn-whatsapp:hover {
        background-color: var(--main2);
    }

    .middle {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background-color: var(--dark);
        padding-top: 2rem;
    }
    .mid {
        min-height: 7vh;
        width: 78%;
        padding: 10px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
    }
    .sub-titulo {
        text-align: center;
        font-family:'Raleway';
        text-shadow: 1px 2px 5px var(--main2);
    }
    .sub-titulo-1 {
        font-size: 3vw;
        color: var(--main3);
    }
    .sub-titulo-2 {
        font-size: 4vw;
        color: var(--light);
    }

    @media (max-width: 900px) {
        .slider {
            width: 100%;
        }
        .space {
            min-height: 4.5vh;
        }
        .sub-titulo {
            font-size: 6vw;
        }
    }

    @media screen and (max-width: 300px) {
        .sub-titulo {
            font-size: 5vw;
        }
    }

    @media screen and (min-width: 500px) {
        .titulos {
            width: 90%;
        }
        .cta-botones {
            margin-top: 2vh;
        }
        .cta-botones a {
            padding: 8px 26px;
            font-size: 1rem;
        }
        .telefono-logo {
            width: 26px;
        }
        .whatsapp-logo {
            width: 26px;
        }
    }

    @media screen and (min-width: 750px) {
        .titulos {
            width: 80%;
        }
        .cta-botones {
            margin-top: 3vh;
        }
        .cta-botones a {
            padding: 11px 32px;
            font-size: 1.6rem;
            border-radius: 8px;
            box-shadow: 2px 2px 16px rgba(0,0,0,0.8);
        }
        .telefono-logo {
            width: 26px;
        }
        .whatsapp-logo {
            width: 26px;
        }
    }

    @media screen and (min-width: 950px) {
        .cta-botones a {
            padding: 16px 40px;
            font-size: 2rem;
        }
    }
</style>
