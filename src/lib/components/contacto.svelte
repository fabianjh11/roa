<script>
    let nombre = "";
    let telefono = "";
    let tipoCaso = "";
  
    function enviarWhatsApp() {
      const numeroEmpresa = "3331727807";
      const texto = `Hola, quiero solicitar una llamada.%0A
                    Nombre: ${encodeURIComponent(nombre)}%0A
                    Teléfono: ${encodeURIComponent(telefono)}%0A
                    Tipo de caso: ${encodeURIComponent(tipoCaso)}`;
  
      const url = `https://wa.me/${numeroEmpresa}?text=${texto}`;
      window.open(url, "_blank");
    }
</script>

<div class="contacto">
    <div class="information">
        <div class="text">
            <h5>Cuéntanos tu caso,</h5>
            <p>Te llamamos en 30 minutos.</p>
        </div>
    </div>
    <div class="formulario">
        <div class="contacto-container">
            <h5 class="contacto-title">Solicita tu llamada</h5>
          
            <form class="contacto-form" on:submit|preventDefault={enviarWhatsApp}>
              <div class="form-group">
                <input id="nombre" type="text" placeholder="Nombre" bind:value={nombre} required />
              </div>
          
              <div class="form-group">
                <input id="telefono" type="tel" placeholder="Teléfono" bind:value={telefono} required />
              </div>
          
              <div class="form-group">
                <input id="tipoCaso" type="text" placeholder="Tipo de caso" bind:value={tipoCaso} required />
              </div>
          
              <button type="submit" class="btn-enviar">Solicitar llamada</button>
            </form>
        </div>
    </div>
</div>

  
<style>
    .contacto {
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 6rem 2rem;
        background-color: var(--main);
    }

    .information {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
    }

    .text {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        padding: 1.6rem;
        color: var(--light);
        text-shadow: 2px 8px 16px var(--dark);
    }

    h5 {
        font-size: 2.6rem;
    }
    p {
        font-size: 1.6rem;
    }

    .formulario {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;

        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
        color: var(--light);
    }

    .contacto-container {
        width: 80%;
        padding: 2rem;
        background-color: var(--dark);
        box-shadow: 2px 8px 16px rgba(0,0,0,0.7);
    }
  
    .contacto-title {
        font-size: 1.6rem;
        margin-bottom: 1rem;
        text-align: center;
    }
  
    .contacto-form {
        display: flex;
        flex-direction: column;
        gap: 1.2rem;
    }
  
    .form-group {
        display: flex;
        flex-direction: column;
    }
  
    input {
        padding: 0.6rem 1rem;
        border: none;
        border-radius: 26px;
        font-size: 1rem;
        color: var(--light);
        background-color: var(--main);
    }
    input:focus {
        border: none;
        background-color: var(--dark);
    }

    input::placeholder {
        color: var(--light);
        opacity: 0.7;
    }
  
    .btn-enviar {
        font-size: 1rem;
        font-weight: bold;
        padding: 0.6rem;
        border: none;
        border-radius: 26px;
        cursor: pointer;

        font-family: 'Montserrat', sans-serif;
        color: var(--dark);
        background-color: var(--main2);
        transition: background 0.3s;
    }
    .btn-enviar:hover {
         background-color: var(--main3);
    }

    @media screen and (min-width: 650px) {
        .contacto {
            flex-direction: row;
            justify-content: center;
            padding: 6rem 2rem;
        }
        .information {
            justify-content: flex-end;
            align-items: center;
            width: 50%;
        }
        h5 {
            font-size: 3.2rem;
        }
        p {
            font-size: 2.6rem;
        }
        .formulario {
            width: 50%;
            justify-content: flex-start;
            align-items: center;
        }
        .contacto-container {
            width: 60%;
            padding: 2rem;
            background-color: var(--dark);
            box-shadow: 2px 8px 16px rgba(0,0,0,0.7);
        }
        .contacto-title {
            font-size: 2.6rem;
            margin-bottom: 1.5rem;
        }
        .btn-enviar {
            font-size: 1.2rem;
            padding: 0.8rem;
        }
    }
</style>
  