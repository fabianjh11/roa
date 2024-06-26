<script>
    import { onMount } from 'svelte';
    import Foto1 from '../assets/foto1.jfif'
    import Foto2 from '../assets/foto2.jfif'
    import Foto3 from '../assets/foto4.jfif'
    import Foto4 from '../assets/foto5.jfif'

    var currentSlide = 0;
    const slideDuration = 5000;

    const images = [
        Foto1,
        Foto2,
        Foto3,
        Foto4
    ];

    function changeSlide(index) {
        currentSlide = index;
        for(var i = 0; i < images.length; i++) {
            if (i == currentSlide) {
                document.getElementById(i).classList.add('selected');
            }
            else {
                document.getElementById(i).classList.remove('selected');
            }
        }
        scrollToSlide(index);
    }

    function scrollToSlide(index) {
        const slider = document.querySelector(".slider-images");
        slider.scrollLeft = index * slider.offsetWidth;
    }

    function autoChangeSlide() {
        const totalSlides = images.length;
        currentSlide = (currentSlide + 1) % totalSlides;
        changeSlide(currentSlide);
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
                {#each images as image, index}
                    {#if index == 0}
                        <img src={image} class="cover-0" alt="fotografía" />
                    {:else if index == 1}
                        <img src={image} class="cover-1" alt="fotografía" />
                    {:else}
                        <img src={image} alt="fotografía" />
                    {/if}
                {/each}
            </div>
            <div class="slider-nav">
                {#each images as _, index}
                    <!-- svelte-ignore a11y-invalid-attribute -->
                    {#if index == 0}
                        <a href="#" class="no-cover selected" id={index} on:click={() => changeSlide(index)}><div></div></a>
                    {:else}
                        <a href="#" id={index} on:click={() => changeSlide(index)}><div></div></a>
                    {/if}
                    
                {/each}
            </div>
        </div>
    </div>
</main>

<style>
    .slider-container {
        max-height: 100vh;
        background: radial-gradient(circle, var(--main) 60%, var(--dark) 100%);
    }
    .slider-wrapper{
        position: relative;
        width: 100%;
        margin: 0 auto;
        overflow: hidden;
        max-height: 90vh;
    }

    .slider-images{
        display: flex;
        aspect-ratio: 16 / 9;
        overflow-x: hidden;
        scroll-snap-type: x mandatory;
        scroll-behavior: smooth;
        box-shadow: 0 1.5rem 3rem -0.75rem hsla(0, 0%, 0%, 0.5);
    }

    .slider-images img{
        flex: 1 0 100%;
        scroll-snap-align: start;
        object-fit: contain;
        overflow: hidden;
        opacity: .8;
    }

    .slider-images .cover-0{
        flex: 1 0 100%;
        scroll-snap-align: start;
        object-fit: cover;
        object-position: 100% 30%;
        overflow: hidden;
        opacity: .8;
    }

    .slider-images .cover-1 {
        flex: 1 0 100%;
        scroll-snap-align: start;
        object-fit: fill;
        overflow: hidden;
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
        background-color: var(--light);
        opacity: 0.75;
        transition: opacity ease 250ms;
    }

    .slider-nav a:hover{
        opacity: 1;
    }
    
    .slider-nav .selected{
        background-color: var(--main);
    }

</style>