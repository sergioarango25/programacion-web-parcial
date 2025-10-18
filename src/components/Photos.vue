<template>
  <div class="photos-layout-grid">
    
    <div class="barra-lateral-perfil">
      
      <div>
        <img
          src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
          alt="Usuario"
          id="foto2"
        />
      </div>

      <div class="seccion-info-lateral">
        <hr>
        <p>Informacion</p>
        <hr />
        <p>Info</p>
        <p>X Amigos</p>
        <p>Ver todos</p>
      </div>

      <div class="fotos-amigos-lateral">
        <img
          src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
          alt="amigos fotos usuario"
          class="amigo"
        />
        <img
          src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
          alt="amigos fotos usuario"
          class="amigo"
        />
        <img
          src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
          alt="amigos fotos usuario"
          class="amigo"
        />
      </div>
    </div>
    
    <div class="contenido-principal-photos">
      
      <h2>Photos</h2>
      <hr class="linea-titulo">

      <div class="galeria-fotos">
        <div class="caja-foto"></div>
        <div class="caja-foto"></div>
        <div class="caja-foto"></div>
        <div class="caja-foto"></div>
      </div>
    
    </div> 
  </div>
</template>

<style scoped>
.photos-layout-grid {
    display: flex;
    justify-content: center;
    width: 100%;
    gap: 40px; 
    padding: 20px 0;
}

.barra-lateral-perfil {
    width: 250px;
    align-self: flex-start;
}

.contenido-principal-photos {
    flex-grow: 1;
    max-width: 650px;
    align-self: flex-start;
    padding: 0 20px;
}

.contenido-principal-photos h2 {
    color: #4267B2;
    margin-top: 0;
    margin-bottom: 5px;
}

.linea-titulo {
    border: none;
    border-top: 1px solid #e0e0e0;
    margin-bottom: 20px;
}



.seccion-info-lateral {
    font-size: 19px;
    margin-top: 20px;
    width: 200px;
}

.seccion-info-lateral p {
    margin: 8px 0;
}

#foto2 {
    margin-top: 0;
    height: 100px;
    width: 100px;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.3);
}

.fotos-amigos-lateral {
    margin-top: 10px;
    width: 100px;
}

.amigo {
    height: 45px;
    width: 45px;
    border: 2px solid white;
    display: inline-block;
    object-fit: cover;
}



.galeria-fotos {
    display: grid;
    grid-template-columns: repeat(4, 1fr); 
    gap: 10px;
    width: 100%;
}

.caja-foto {

    width: 100%;
    padding-top: 100%; 
    background-color: #4267B2;
    border: 1px solid white;
    box-shadow: 0 0 5px 5px rgba(0, 0, 0, 0.3);
    border-radius: 3px;
    position: relative;
}
</style>