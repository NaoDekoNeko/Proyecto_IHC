<template>
  <div class="conocenos-web">
    
    <div class="container">
      <div class="image-19"></div>
      <div class="educational-virtual-assistant">
        Educational Virtual Assistant
      </div>
      <div class="frame-2610367">
        <span class="text1">
          ¡Bienvenido a la sección 'Conócenos'! Permíteme presentarte a los creadores detrás de esta plataforma. Somos un equipo apasionado de desarrolladores dedicados a proporcionarte la mejor experiencia de aprendizaje en línea. Desde el diseño hasta la implementación, hemos trabajado arduamente para crear una plataforma que se adapte a tus necesidades educativas. ¡Esperamos que disfrutes de lo que hemos creado para ti!
        </span>
        <div class="image-12"></div>
      </div>
      <div class="large-grid">
        <div class="card">
          <div class="graphic"></div>
          <div class="copy">
            <span class="pool-lsalvatierra-a">
              Pool L. Salvatierra A.
            </span>
            <span class="ceo-yfundador-de-eva-corporation">
              CEO y fundador de EVA corporation. 
            </span>
          </div>
        </div>
        <div class="card-1">
          <div class="image"></div>
          <div class="copy-1">
            <span class="manuel-afatama-r">
              Manuel A. Fatama R.
            </span>
            <span class="arquitecto-cloud">
              Arquitecto Cloud 
            </span>
          </div>
        </div>
        <div class="card-2">
          <div class="image-1"></div>
          <div class="copy-2">
            <span class="bruno-gcipriano-a">
              Bruno G. Cipriano A.
            </span>
            <span class="desarrollador-web">
              Desarrollador WEB
            </span>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'ConocenosWeb'
}
</script>

<style scoped>
html, body {
  height: 100%;
  margin: 0;
}

#app {
  height: 100%;
}

.conocenos-web {
  background: #D6FFFF;
  display: flex;
  flex-direction: column;
  padding: 30px 20.2px 8.5px 35px;
  min-width: 190vh;
  min-height: 90vh; /* Asegura que cubra toda la altura de la página */
  box-sizing: border-box;
}

.image-10, .image-12 {
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}

.container {
  text-align: center;
  margin-top: 50px;
}

.large-grid {
  display: flex;
  gap: 20px;
}

.card {
  border: 1px solid #ccc;
  padding: 20px;
  text-align: left;
}

.card .graphic, .card-1 .image, .card-2 .image-1 {
  height: 232px;
  background-color: #e0e0e0;
}

.card .copy, .copy-1, .copy-2 {
  margin-top: 10px;
}

.pool-lsalvatierra-a {
  font-weight: bold;
}

.ceo-yfundador-de-eva-corporation {
  font-style: italic;
}

.educational-virtual-assistant-eva-10 {
  /* Estilos adicionales */
}

.image-19 {
  background: url('../assets/images/image_19.png') 50% / cover no-repeat;
  position: absolute;
  right: 100px;
  bottom: 220px;
  width: 229px;
  height: 260px;
}



.educational-virtual-assistant {
  margin: 0 0 30.5px 23.2px;
  display: inline-block;
  overflow-wrap: break-word;
  font-family: 'Inter';
  font-weight: 600;
  font-size: 24px;
  letter-spacing: -0.2px;
  line-height: 1.5;
  color: #000000;
}

.frame-2610367 {
  border-radius: 16px 16px 0 16px;
  background: #000000;
  margin: 0 0 88px 60.2px;
  display: flex;
  padding: 12px 31.4px 12px 16px;
  box-sizing: border-box;
}

.text1 {
  overflow-wrap: break-word;
  font-family: 'Inter';
  font-weight: 500;
  font-size: 20px;
  width: 900px;

  line-height: 1.5;
  color: #FFFFFF;
}

.graphic {
  border-radius: 8px;
  background: url('../assets/images/graphic.jpeg') 50% / cover no-repeat, linear-gradient(#B5DBFF, #B5DBFF);
  margin-bottom: 12px;
  width: 232px;
  height: 232px;
}

.pool-lsalvatierra-a {
  overflow-wrap: break-word;
  font-family: 'Inter';
  font-weight: 500;
  font-size: 20px;
  line-height: 1.5;
  color: #000000;
}

.ceo-yfundador-de-eva-corporation {
  margin-right: 17.9px;
  overflow-wrap: break-word;
  font-family: 'Inter';
  font-weight: 400;
  font-size: 16px;
  line-height: 1.5;
  color: #454545;
}

.copy {
  display: flex;
  flex-direction: column;
  align-items: center;
  align-self: flex-start;
  width: fit-content;
  box-sizing: border-box;
}

.card {
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
}

.image {
  border-radius: 8px;
  background: url('../assets/images/image.jpeg') 50% / cover no-repeat, linear-gradient(#FFEE93, #FFEE93);
  margin-bottom: 12px;
  width: 232px;
  height: 232px;
}

.manuel-afatama-r {
  overflow-wrap: break-word;
  font-family: 'Inter';
  font-weight: 500;
  font-size: 20px;
  line-height: 1.5;
  color: #000000;
}

.arquitecto-cloud {
  align-self: flex-start;
  overflow-wrap: break-word;
  font-family: 'Inter';
  font-weight: 400;
  font-size: 16px;
  line-height: 1.5;
  color: #454545;
}

.copy-1 {
  display: flex;
  flex-direction: column;
  align-self: flex-start;
  width: fit-content;
  box-sizing: border-box;
}

.card-1 {
  margin-bottom: 24px;
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
}

.image-1 {
  border-radius: 8px;
  background: url('../assets/images/image_1.jpeg') 50% / cover no-repeat, linear-gradient(#FFC1C1, #FFC1C1);
  margin-bottom: 12px;
  width: 232px;
  height: 232px;
}

.bruno-gcipriano-a {
  overflow-wrap: break-word;
  font-family: 'Inter';
  font-weight: 500;
  font-size: 20px;
  line-height: 1.5;
  color: #000000;
}

.desarrollador-web {
  align-self: flex-start;
  overflow-wrap: break-word;
  font-family: 'Inter';
  font-weight: 400;
  font-size: 16px;
  line-height: 1.5;
  color: #454545;
}

.copy-2 {
  display: flex;
  flex-direction: column;
  align-self: flex-start;
  width: fit-content;
  box-sizing: border-box;
}

.card-2 {
  margin-bottom: 24px;
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
}

.large-grid {
  margin: 0 0 55.5px 25.2px;
  display: flex;
  flex-direction: row;
  column-gap: 32px;
  width: fit-content;
  box-sizing: border-box;
}

.educational-virtual-assistant-eva-10 {
  align-self: flex-end;
  overflow-wrap: break-word;
  font-family: 'Inter';
  font-weight: 600;
  font-size: 24px;
  letter-spacing: -0.2px;
  line-height: 1.5;
  color: rgba(0, 0, 0, 0.5);
}

.container {
  background: #D6FFFF;
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-sizing: border-box;
}
</style>
