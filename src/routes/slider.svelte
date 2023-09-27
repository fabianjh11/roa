<script>
    import { onMount } from 'svelte';
    import Foto1 from '../assets/foto1.jpg'
    import Foto2 from '../assets/foto2.jpg'
    import Foto3 from '../assets/foto3.jpg'
    import Foto4 from '../assets/foto4.jpg'
    import Foto5 from '../assets/foto5.jpg'
    import Foto6 from '../assets/foto6.jpg'

    let currentSlide = 0;
    const slideDuration = 5000;

    const images = [
        Foto2,
        Foto1,
        Foto4,
        Foto5,
        Foto6
    ];

    function changeSlide(index) {
        currentSlide = index;
        scrollToSlide(index);
    }

    function scrollToSlide(index) {
        const slider = document.querySelector(".slider-images");
        slider.scrollLeft = index * slider.offsetWidth;
    }

    function autoChangeSlide() {
        const totalSlides = images.length;
        currentSlide = (currentSlide + 1) % totalSlides;
        scrollToSlide(currentSlide);
    }

    onMount(() => {
        const sliderInterval = setInterval(autoChangeSlide, slideDuration);
        return () => {
        clearInterval(sliderInterval);
        };
    });
</script>

<main>
    <div class="slider-container">
        <div class="slider-wrapper">
            <div class="slider-images" >
                {#each images as image}
                    <img src={image} alt="" />
                {/each}
            </div>
            <div class="slider-nav">
                {#each images as _, index}
                    <!-- svelte-ignore a11y-invalid-attribute -->
                    <a href="#" on:click={() => changeSlide(index)}><div></div></a>
                {/each}
            </div>
        </div>
    </div>
</main>

<style>
    .slider-wrapper{
        position: relative;
        width: 100%;
        margin: 0 auto;
        overflow: hidden;
    }

    .slider-images{
        display: flex;
        aspect-ratio: 16 / 9;
        overflow-x: auto;
        scroll-snap-type: x mandatory;
        scroll-behavior: smooth;
        box-shadow: 0 1.5rem 3rem -0.75rem hsla(0, 0%, 0%, 0.5);

    }

    .slider-images img{
        flex: 1 0 100%;
        scroll-snap-align: start;
        object-fit: cover;
        opacity: .8;
    }

    .slider-nav{
        display: flex;
        column-gap: 1rem;
        position: absolute;
        bottom: 1.25rem;
        left: 50%;
        transform: translateX(-50%);
        z-index: 1;
    }

    .slider-nav a{
        width: 0.5rem;
        height: 0.5rem;
        border-radius: 50%;
        background-color: #fff;
        opacity: 0.75;
        transition: opacity ease 250ms;
    }

    .slider-nav a:hover{
        opacity: 1;
    }

</style>