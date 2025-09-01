<script>
    export let materia = "";
    import Penal from "../../assets/penal.jpg";
    import Familiar from "../../assets/familiar.jpg";
    import Civil from "../../assets/civil.jpg";
    import Mercantil from "../../assets/mercantil.jpg";
    import Corporativo from "../../assets/corporativo.jpg";
    import Laboral from "../../assets/laboral.jpg";
</script>

<main>
    {#if materia == "m1"}
    <div id="m1" class="materia" >
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div class="content" on:click|stopPropagation>
            <div class="relative">
                <h6>Penal</h6>
                <img src={Penal} alt="">
            </div>
            <ul>
                <li>Fraude</li>
                <li>Abuso de confianza</li>
                <li>Robo</li>
                <li>Despojos</li>
                <li>Violencia familiar</li>
                <li>Delitos sexuales</li>
                <li>Amparo y Apelaciones</li>
            </ul>
        </div>
        <div class="contactar">
            <a href="https://api.whatsapp.com/send?phone=3331727807&text=Hola%2C%20vengo%20del%20sitio%20web%20ROA%20CORPORATIVO%20JURIDICO%2C%20quisiera%20brindar%20información%20sobre%20mi%20asunto%20en%20materia%20Penal%2E" target="_blank" class="btn-whatsapp">
                <svg class="whatsapp-logo" xmlns="http://www.w3.org/2000/svg" width="8vw" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                    <path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/>
                </svg>
                Resolver mi caso
            </a>
        </div>  
    </div>
    {:else if materia == "m2"}
    <div id="m2" class="materia">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div class="content" on:click|stopPropagation>
            <div class="relative">
                <h6>Familiar</h6>
                <img src={Familiar} alt="">
            </div>
            <ul>
                <li>Divorcios</li>
                <li>Pensión alimenticia</li>
                <li>Custodia</li>
                <li>Convivencia</li>
                <li>Pérdida de Patria Potestad</li>
                <li>Reconocimiento de Paternidad</li>
                <li>Desconocimiento de Paternidad</li>
                <li>Sucesiones</li>
                <li>Interdictos</li>
                <li>Amparos y Apelaciones</li>
            </ul>
        </div>
        <div class="contactar">
            <a href="https://api.whatsapp.com/send?phone=3331727807&text=Hola%2C%20vengo%20del%20sitio%20web%20ROA%20CORPORATIVO%20JURIDICO%2C%20quisiera%20brindar%20información%20sobre%20mi%20asunto%20en%20materia%20Familiar%2E" target="_blank" class="btn-whatsapp">
                <svg class="whatsapp-logo" xmlns="http://www.w3.org/2000/svg" width="8vw" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                    <path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/>
                </svg>
                Resolver mi caso
            </a>
        </div>
    </div>
    {:else if materia == "m3"}
    <div id="m3" class="materia">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div class="content" on:click|stopPropagation>
            <div class="relative">
                <h6>Civil</h6>
                <img src={Civil} alt="">
            </div>
            <ul>
                <li>Contratos (compraventa, arrendamiento, comodato)</li>
                <li>Usucapión</li>
                <li>Acción proforma</li>
                <li>Reivindicatoria</li>
                <li>Amparos y Apelaciones</li>
            </ul>
        </div>
        <div class="contactar">
            <a href="https://api.whatsapp.com/send?phone=3331727807&text=Hola%2C%20vengo%20del%20sitio%20web%20ROA%20CORPORATIVO%20JURIDICO%2C%20quisiera%20brindar%20información%20sobre%20mi%20asunto%20en%20materia%20Civil%2E" target="_blank" class="btn-whatsapp">
                <svg class="whatsapp-logo" xmlns="http://www.w3.org/2000/svg" width="8vw" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                    <path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/>
                </svg>
                Resolver mi caso
            </a>
        </div>
    </div>
    {:else if materia == "m4"}
    <div id="m4" class="materia">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div class="content" on:click|stopPropagation>
            <div class="relative">
                <h6>Mercantil</h6>
                <img src={Mercantil} alt="">
            </div>
            <ul>
                <li>Pagarés</li>
                <li>Contratos mercantiles</li>
                <li>Seguros</li>
                <li>Amparos y Apelaciones</li>
            </ul>
        </div>
        <div class="contactar">
            <a href="https://api.whatsapp.com/send?phone=3331727807&text=Hola%2C%20vengo%20del%20sitio%20web%20ROA%20CORPORATIVO%20JURIDICO%2C%20quisiera%20brindar%20información%20sobre%20mi%20asunto%20en%20materia%20Mercantil%2E" target="_blank" class="btn-whatsapp">
                <svg class="whatsapp-logo" xmlns="http://www.w3.org/2000/svg" width="8vw" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                    <path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/>
                </svg>
                Resolver mi caso
            </a>
        </div>
    </div>
    {:else if materia == "m5"}
    <div id="m5" class="materia">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div class="content" on:click|stopPropagation >
            <div class="relative">
                <h6>Corporativo</h6>
                <img src={Corporativo} alt="">
            </div>
            <ul>
                <li>Creación de sociedades</li>
                <li>Libros societarios</li>
                <li>Actas de asamblea</li>
                <li>Registro de marcas</li>
                <li>Declaración de uso de marcas</li>
            </ul>
        </div>
        <div class="contactar">
            <a href="https://api.whatsapp.com/send?phone=3331727807&text=Hola%2C%20vengo%20del%20sitio%20web%20ROA%20CORPORATIVO%20JURIDICO%2C%20quisiera%20brindar%20información%20sobre%20mi%20asunto%20en%20materia%20Corporativa%2E" target="_blank" class="btn-whatsapp">
                <svg class="whatsapp-logo" xmlns="http://www.w3.org/2000/svg" width="8vw" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                    <path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/>
                </svg>
                Resolver mi caso
            </a>
        </div>
    </div>
    {:else if materia == "m6"}
    <div id="m6" class="materia">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div class="content" on:click|stopPropagation>
            <div class="relative">
                <h6>Laboral</h6>
                <img src={Laboral} alt="">
            </div>
            <ul>
                <li>Despidos injustificados</li>
                <li>Contratos laborales</li>
                <li>Cumplimiento de prestaciones</li>
                <li>Amparo en Materia Laboral</li>
            </ul>
        </div>
        <div class="contactar">
            <a href="https://api.whatsapp.com/send?phone=3331727807&text=Hola%2C%20vengo%20del%20sitio%20web%20ROA%20CORPORATIVO%20JURIDICO%2C%20quisiera%20brindar%20información%20sobre%20mi%20asunto%20en%20materia%20Laboral%2E" target="_blank" class="btn-whatsapp">
                <svg class="whatsapp-logo" xmlns="http://www.w3.org/2000/svg" width="8vw" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                    <path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/>
                </svg>
                Resolver mi caso
            </a>
        </div>
    </div>
    {/if}
</main>

<style>
    :root {
        --dark: #182322;
        --light: #F5F6EB;
        --main: #047E8E;
        --contrast: #CDE49A;
        --main2: #8ACED2;
    }
    .materia {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        position: fixed;
        top: 50%;
        bottom: 50%;
        left: 0;
        width: 100%;
        height: 100%;
        margin: auto;
        z-index: 10;
        background-color: #0008;
    }
    .relative {
        position: relative;
        width: 290px;
        height: 100px;
        display: flex;
    }
    img {
        object-fit: cover;
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        opacity: .7;
        border-radius: 2vw;
    }
    h6 {
        position: relative;
        text-align: center;
        font-size: 35px;
        color: var(--light);
        z-index: 1;
        margin: auto;
    }
    .content {
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-evenly;
        width: 300px;
        padding: 20px;
        background-color: var(--dark);
        border-radius: 2vw;
        box-shadow: 0 1.5rem 3rem -0.75rem hsla(0, 0%, 0%, 1);
    }
    ul {
        display: flex;
        flex-direction: column;
        z-index: 3;
        max-width: 290px;
        list-style: circle;
        justify-content: center;
        padding: 30px;
    }
    li {
        font-size: 20px;
        padding: 1px;
        color: var(--light);
    }

    .contactar {
        margin-top: 1.5rem;
        font-family: 'Raleway', sans-serif;
    }
    .contactar a {
        display: flex;
        gap: 8px;
        justify-content: center;
        align-items: center;
        
        padding: .8rem 1.8rem;
        font-size: 1.2rem;
        font-weight: bolder;
        border-radius: 8px;
        text-decoration: none;

        background-color: var(--light);
        color: var(--main);
        box-shadow: 1px 1px 8px rgba(0,0,0,0.8);
        transition: all 0.3s ease;
    }
    .contactar a:hover {
        background-color: var(--main3);
    }
    .whatsapp-logo {
        fill: var(--main);
        width: 16px;
    }

    @media screen and (max-width: 300px) {
        .relative {
            max-width: 250px;
        }
        .content {
            width: 260px;
        }
        h6 {
            font-size: 30px;
        }
        ul {
            max-width: 220px;
            font-size: 15px;
        }
    }
    
</style>