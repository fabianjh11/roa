<script>
</script>

<div class="navbar">
    <div class="items">
        <h4 class="t-navbar"><a href="#inicio">ROA</a></h4>

        <div class="contactar">
            <a href="tel:+3331727807">
                <svg class="telefono-logo" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 640">
                    <!--!Font Awesome Free v7.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.-->
                    <path d="M224.2 89C216.3 70.1 195.7 60.1 176.1 65.4L170.6 66.9C106 84.5 50.8 147.1 66.9 223.3C104 398.3 241.7 536 416.7 573.1C493 589.3 555.5 534 573.1 469.4L574.6 463.9C580 444.2 569.9 423.6 551.1 415.8L453.8 375.3C437.3 368.4 418.2 373.2 406.8 387.1L368.2 434.3C297.9 399.4 241.3 341 208.8 269.3L253 233.3C266.9 222 271.6 202.9 264.8 186.3L224.2 89z"/>
                </svg>
                Consulta inicial sin costo
            </a>
        </div>
    </div>
</div>

<style>
    .navbar{
        background: linear-gradient(to left, var(--dark), var(--main));
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        padding: 10px;
        height: 50px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        z-index: 5;
    }

    .items{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
        width: 100%;
    }

    .t-navbar, .t-navbar a{
        padding-left: 1%;
        font-size: 3vh;
        text-decoration: none;
        color: var(--light);
        cursor: pointer;
    }

    .contactar {
        padding-right: 8%;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    .contactar a {
        color: var(--light);
        text-decoration: none;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 11px;
        gap: 8px;
    }
    .contactar:hover a {
        color: #c0cdcd;
    }
    .telefono-logo {
        fill: var(--light);
        width: 16px;
    }
    .contactar:hover .telefono-logo {
        fill: #c0cdcd;
    }

    @media screen and (min-width: 750px) {
        .contactar {
            padding-right: 3%;
        }
        .contactar a {
            font-size: 16px;
        }
        .telefono-logo {
            width: 22px;
        }
    }
</style>