<template>
  <div class="info-layout-grid">
    
    <div class="barra-lateral-perfil">
      
      <div>
        <img
          src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
          alt="usuario"
          id="foto2"
        />
      </div>

      <div class="seccion-info-lateral">
        <hr>
        <p>Informacion</p>
        <hr />
        <p>Email</p>
        <p>Telefono</p>
        <p>Intereses</p>
        <p>Situacion Sentimental</p>
        <p>Ver todos..</p>
      </div>

      <div class="fotos-amigos-lateral">
        <img
          src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
          alt="amigos fotos usuario"
          class="amigo-img"
        />
      </div>
    </div>
    
    <div class="contenido-principal">
      <div class="tarjeta-detalles-info">
        
        <div class="info-seccion-cabecera">
          <h2>Info</h2>
          <hr>
          <p>Email</p>
          <p>Telefono</p>
          <p>Intereses</p>
          <p>Situacion sentimental</p>
        </div>

        <div class="info-seccion-pie">
          <img
            src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
            alt="Perfil Pequeño"
            class="info-avatar-pequeno"
          />
          <div class="info-bloque-texto">
            <p class="info-texto-nombre">Emal</p>
            <p class="info-texto-fecha">70 abr</p>
          </div>
          <div class="info-acciones">
            <button class="btn-me-gusta">👍 Me gusta</button>
            <button class="btn-compartir">💬 Compartir</button>
          </div>
        </div>

      </div>
    </div> 
  </div>
</template>

<script>
export default {
  name: 'Info'
}
</script>

<style scoped>
.info-layout-grid {
    display: flex;
    justify-content: center; 
    width: 100%;
    gap: 100px; 
    padding: 20px 0;
}

.barra-lateral-perfil {
    width: 250px; 
    align-self: flex-start; 
}

.contenido-principal {
    flex-grow: 1; 
    max-width: 650px; 
    align-self: flex-start;
}


.seccion-info-lateral {
    font-size: 19px;
    margin-top: 30px;
    width: 200px;
}

.seccion-info-lateral p {
    margin: 8px 0;
}

#foto2 {
    margin-top: 0;
    height: 100px;
    width: 100px;
}

.fotos-amigos-lateral {
    margin-top: 10px;
    width: 100px;
}

.amigo-img {
    height: 45px;
    width: 45px;
    border: 2px solid white; 
}


.tarjeta-detalles-info {
    background-color: white;
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 20px;
}

.info-seccion-cabecera h2 {
    color: #4267B2;
    margin-top: 0;
    margin-bottom: 5px;
}

.info-seccion-cabecera hr {
    border: none;
    border-top: 1px solid #e0e0e0;
    margin-bottom: 20px;
}

.info-seccion-cabecera p {
    margin: 8px 0;
    font-size: 16px;
    color: #333;
}

.info-seccion-pie {
    display: grid;
    grid-template-columns: 40px 1fr;
    gap: 10px;
    align-items: center;
    margin-top: 15px;
    border-top: 1px solid #e0e0e0;
    padding-top: 20px;
}

.info-avatar-pequeno {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    object-fit: cover;
    background-color: #ccc;
    grid-column: 1;
}

.info-bloque-texto {
    grid-column: 2; 
    grid-row: 1 / span 2; 
}

.info-texto-nombre {
  font-size: 25px;
  color: #4267B2;
  margin: 0;
}

.info-texto-fecha {
    font-size: 12px;
    color: #606770;
    margin: 0;
}

.info-acciones {
    grid-column: 1 / span 2;
    display: flex;
    justify-content: flex-start;
    gap: 10px;
    margin-top: 15px;
}

.btn-me-gusta, .btn-compartir {
    background-color: #e4e6eb;
    font-size: 20px;
    color: #4267B2;
    border: 1px solid #ccd0d5;
    padding: 8px 12px;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
    display: flex; 
    align-items: center;
    gap: 5px;
}

</style>