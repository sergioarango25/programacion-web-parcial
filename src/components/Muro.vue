<template>
  <div>
    <img
      src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
      alt="Imagen de ejemplo"
      id="foto2"
    />
  </div>

  <div class="muro">
    <p>Adjuntar</p>
    <hr />
    <p>Compartir</p>
    <hr />

    <div class="amigos-area">
      <p class="amigos-label">X Amigos</p>

      <div class="fotos-amigos">
        <img
          src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
          alt="amigos fotos usuario"
          class="amigo-img"
        />
        <img
          src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
          alt="amigos fotos usuario"
          class="amigo-img"
        />
        <img
          src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
          alt="amigos fotos usuario"
          class="amigo-img"
        />
      </div>
    </div>
  </div>

  <div class="muro-container">
    <div class="input-caja">
      <input
        type="text"
        placeholder="Pon algo aquí..."
        class="contenido-publicacion"
      />

      <div class="actions">
        <p class="adjuntar">Adjuntar ➕</p>
        <button class="compartir-btn">Compartir</button>
      </div>
    </div>

    <div class="caja-contenido">
      <div class="carta">
        <div class="header-carta">
          <p class="header-contenido">Muro + Otros</p>
          <p class="header-contenido">Solo Nombre</p>
        </div>

        <div class="contenido-publicacion">
          <img
            src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
            alt="Perfil"
            class="perfil"
          />

          <div class="detalles">
            <p class="nombre">Nombre</p>
            <p class="tiempo">Lunes a las 8:45pm - Me gusta</p>
          </div>
        </div>

        <div class="comentarios">
          <hr />
          <p class="ver-comentarios">Ver los 6 comentarios</p>
          <hr />
        </div>

        <div class="caja-comenatarios">
          <img
            src="https://i.pinimg.com/736x/0f/68/94/0f6894e539589a50809e45833c8bb6c4.jpg"
            alt="Comentario Avatar"
            class="comment-avatar"
          />
          <div class="comentarios-usuarios">
            <p class="nombre-comentario">Nombre</p>
            <p class="tiempo-comentario">Lunes a las 11:46pm</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.muro {
  position: absolute;
  top: 80%;
  left: 9%;
  transform: translate(-50%, -50%);
  gap: 2%;
  font-size: 20px;
  margin: 5px;
}

#foto2 {
  margin-top: -10px;
  height: 200px;
  width: 200px;
}

.amigos-area {
  display: flex;
  flex-direction: column;
  margin-top: 10px;
}

.amigos-label {
  margin: 0;
}

.fotos-amigos {
  display: flex;
  margin-top: 10px;
  margin-left: -10px;
}

.amigo-img {
  display: flex;
  gap: 20px;
  height: 45px;
  width: 45px;
  border: 2px solid white;
}

.muro-container {
  padding: 20px;
  margin-left: 250px;
  max-width: 600px;
}

.input-caja {
  position: relative;
  top: 20%;
  left: 50%;
  transform: translate(-20%, -50%);
  background-color: white;
  border: 1px solid #ddd;
  padding: 10px;
  border-radius: 5px;
  margin-top: -150px;
}

.caja-contenido {
  position: relative;
  top: -50%;
  left: 50%;
  transform: translate(-20%, -50%);
  background-color: white;
  padding: 10px;
  border-radius: 5px;
  margin-top: 20%;
}

.contenido-publicacion {
  width: 100%;
  padding: 8px;
  border-radius: 3px;
  margin-bottom: 10px;
  box-sizing: border-box;
}

.actions {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.adjuntar {
  color: #4267b2;
  cursor: pointer;
  font-size: 14px;
  margin: 0;
}

.compartir-btn {
  background-color: #4267b2;
  color: white;
  border: none;
  padding: 5px 15px;
  border-radius: 3px;
  cursor: pointer;
  font-weight: bold;
}

.carta {
  background-color: white;
  border: 1px solid #ddd;
  padding: 15px;
  border-radius: 5px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
}

.header-carta {
  display: flex;
  gap: 15px;
  margin-bottom: 15px;
  color: #4267b2;
  font-size: 14px;
}

.contenido-publicacion,
.caja-comenatarios {
  display: grid;
  grid-template-columns: 50px 2fr;
  gap: 20px;
  align-items: flex-start;
}

.perfil,
.comment-avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  object-fit: cover;
  background-color: #ccc;
}

.detalles,
.comentarios-usuarios {
  padding-top: 5px;
}

.nombre,
.nombre-comentario {
  color: #4267b2;
  margin: 0;
}

.tiempo,
.tiempo-comentario {
  font-size: 12px;
  color: #606770;
  margin: 0;
}

.comentarios {
  margin-top: 15px;
  margin-bottom: 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.comentarios hr {
  border: none;
  border-top: 1px solid #e0e0e0;
  width: 100%;
}

.ver-comentarios {
  color: #4267b2;
  font-size: 14px;
  cursor: pointer;
  padding: 5px 0;
  margin: 5px 0;
}

.caja-comenatarios {
  margin-left: 10px;
  margin-top: 10px;
}

.content-area {
  display: flex;
  justify-content: center;
  width: 100%;
  padding: 20px 0;
  box-sizing: border-box;
}
</style>
