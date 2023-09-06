<script>
    export let materia = "";
    import Penal from "../assets/penal.jpg";
    import Familiar from "../assets/familiar.jpg";
    import Civil from "../assets/civil.jpg";
    import Mercantil from "../assets/mercantil.jpg";
    import Administrativo from "../assets/administrativo.jpg";
    import Laboral from "../assets/laboral.jpg";


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
    </div>
    {:else if materia == "m5"}
    <div id="m5" class="materia">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div class="content" on:click|stopPropagation >
            <div class="relative">
                <h6>Administrativo</h6>
                <img src={Administrativo} alt="">
            </div>
            <ul>
                <li>Nulidad de todo tipo de infracciones</li>
                <li>Órdenes verbales de clausura</li>
                <li>Clausuras de construcciones</li>
                <li>Clausuras de locales y/o negocios</li>
                <li>Licencias de edificación</li>
                <li>Amparo</li>
            </ul>
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