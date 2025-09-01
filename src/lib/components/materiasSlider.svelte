<script>
    import { onMount } from 'svelte';
    import Materias from "./materias.svelte";
    import PenalIcon from './icons/penalIcon.svelte';
    import WorkIcon from './icons/workIcon.svelte';
    import FamilyIcon from './icons/familyIcon.svelte';
    import CivilIcon from './icons/civilIcon.svelte';
    import MercantilIcon from './icons/mercantilIcon.svelte';
    import CorporativeIcon from './icons/corporativeIcon.svelte';

    let materiaSeleccionada = "";
    let id = "";
    let currentSlide = 0;
    const slideDuration = 5000;

    let materias = [
        { id: "m1", titulo: "Derecho Penal", descripcion: "Fraude, robo, delitos.", icono: PenalIcon },
        { id: "m2", titulo: "Derecho Familiar", descripcion: "Divorcios, custodia, sucesiones", icono: FamilyIcon},
        { id: "m3", titulo: "Derecho Civil", descripcion: "Contratos, usucapión, amparos.", icono: CivilIcon},
        { id: "m4", titulo: "Derecho Mercantil", descripcion: "Contratos, pagarés, seguros.", icono: MercantilIcon },
        { id: "m5", titulo: "Derecho Corporativo", descripcion: "Sociedades, marcas, actas.", icono: CorporativeIcon },
        { id: "m6", titulo: "Derecho Laboral", descripcion: "Despidos, contratos, prestaciones.", icono: WorkIcon }
    ];

    // devuelve el índice circular
    function mod(n, m) {
        return ((n % m) + m) % m;
    }

    // obtener el subconjunto actual (3 cards)
    $: visibleMaterias = [
        materias[mod(currentSlide - 1, materias.length)],
        materias[mod(currentSlide, materias.length)],
        materias[mod(currentSlide + 1, materias.length)]
    ];

    function autoChangeSlide() {
        if (materiaSeleccionada != "") return;
        currentSlide = (currentSlide + 1) % materias.length;
    }

    function prev() {
        currentSlide = (currentSlide - 1) % materias.length;
    }
    function next() {
        currentSlide = (currentSlide + 1) % materias.length;
    }

    function handleClick(event) {
        id = event.currentTarget.getAttribute('id');
        materiaSeleccionada = id;
        event.stopPropagation();
    }

    function handleBodyClick() {
        materiaSeleccionada = "";
    }

    onMount(() => {
        document.body.addEventListener('click', handleBodyClick);
        const sliderInterval = setInterval(autoChangeSlide, slideDuration);
        return () => {
            clearInterval(sliderInterval);
            document.body.removeEventListener('click', handleBodyClick);
        };
    });
</script>

<div class="materias-slider">
    <button class="nav left" on:click={prev}>‹</button>
    <div class="slider-wrapper">
        <div class="slider-materias">
            {#each visibleMaterias as m}
                <div class="card">
                    <div class="icon">
                        <svelte:component this={m.icono} color="var(--main)" />
                    </div>
                    <h3>{m.titulo}</h3>
                    <p>{m.descripcion}</p>
                    <button id={m.id} on:click={handleClick}>Saber más</button>
                </div>
            {/each}
        </div>
    </div>
    <button class="nav right" on:click={next}>›</button>

    <Materias materia={materiaSeleccionada} />
</div>

<style>
    .materias-slider {
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        padding: 1rem 0;
        width: 100%;
        overflow: hidden;
        background: var(--dark);
    }

    .slider-wrapper{
        position: relative;
        width: 100%;
        margin: 0 auto;
        overflow: hidden;
    }

    .slider-materias {
        display: flex;
        justify-content: space-between;
        overflow-x: hidden;
        gap: 8px;
        min-height: 25vh;
    }

    .card {
        flex: 0 0 28%;
        border-radius: 16px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        font-size: .7rem;
        color: var(--light);
        text-align: center;
    }

    .icon {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: .6rem;
        width: 50px;
        border-radius: 60px;
        background-color: var(--main2);
    }

    .card button {
        margin-top: 10px;
        padding: 0.4rem .8rem;
        border: none;
        border-radius: 8px;
        font-size: .6rem;
        font-weight: bold;
        background-color: var(--main2);
        color: var(--dark);
        cursor: pointer;
        transition: all .3s ease;
    }
    .card button:hover {
        opacity: .8;
    }

    .nav {
        background: none;
        border: none;
        font-size: 2rem;
        cursor: pointer;
        color: var(--main2);
        padding: 0 .8rem;
    }

    @media screen and (min-width: 500px) {
        .slider-materias {
            min-height: 30vh;
        }

        .card {
            flex: 0 0 30%;
            font-size: .8rem;
        }

        .card button {
            font-size: 1rem;
        }
        .icon {
            padding: .8rem;
            border-radius: 66px;
            width: 72px;
        }
    }

    @media screen and (min-width: 750px) {
        .materias-slider {
            width: 90%;
            padding: 4rem 0;
        }

        .slider-materias {
            min-height: 35vh;
        }

        .card {
            flex: 0 0 30%;
            font-size: 1.2rem;
        }
        .card button {
            font-size: 1rem;
            font-weight: bold;
        }

        .icon {
            padding: .8rem;
            border-radius: 80px;
            width: 90px;
        }

        .nav {
            font-size: 4rem;
            padding: 0 1rem;
        }
    }

    @media screen and (min-width: 950px) {
        .materias-slider {
            width: 86%;
            padding: 4rem 0;
        }

        .slider-materias {
            min-height: 22rem;
        }

        .icon {
            padding: 1.2rem;
            border-radius: 90px;
            width: 110px;
        }
    }
</style>