<template>
  <v-app>
    <div id="firstSection" class="section-format">
      <v-container fluid fill-height>
        <v-layout row align-center>
          <div class="my-flex">
            <v-flex offset-xs2>
              <hr>
            </v-flex>
            <v-flex offset-xs2>
              <h1 id="title">INCORET</h1>
            </v-flex>
            <v-flex xs5>
              <hr>
            </v-flex>
            <v-flex offset-xs2>
              <h2 class="sub-title">INSTALACIÓN CORPORATIVA
              <br>
              DE REDES Y TELEFONÍA
             </h2>
            </v-flex>
          </div>
        </v-layout>
        <img src="@/assets/left_squares.png" alt="squares" class="squares-anim">
      </v-container >
    </div>
    <div id="aboutUs" class="section-format">
      <v-container fluid fill-height class="contain">
        <v-layout row>
          <v-flex offset-(xs1|sm3 mt-4 mr-5()>
            <h2 id="title" class="text-xs-center py-3">NOSOTROS</h2>
            <hr>
            <v-flex class="body text-xs-left text-sm-right text-md-right mt-3 pt-3 pl-5">
              <p>
                Contamos con 11 años de experiencia en el negocio de las telecomunicaciones, ofreciendo  dentro de un
                marco profesional y ético, el soporte  en la entrega de servicios con calidad al usuario final.
              </p>
              <p>
                Estamos enfocados a ser su aliado, para poder alcanzar con garantías,
                los grandes retos que el mercado de las telecomunicaciones exige.
              </p>
            </v-flex>
          </v-flex>
        </v-layout>
      </v-container>
      <img src="@/assets/right_squares.png" alt="squares" class="squares-anim hidden-xs-only" >
    </div>

  </v-app>
</template>

<script>

  export default {
    components: {
    }
  }
</script>

<style>
  #firstSection{
    background-image: url(../assets/1LP.png);

  }
  #title{
    font-size: 55px;
    color: #fff;
    height: 100px;
    font-weight: 700;
  }
  .my-flex{
    display:flex;
    flex-direction: column;
    flex: 1 1 auto;
  }
  .sub-title{
    font-size: 25px;
    color: #fff;
    height: 200px;
    font-weight: 100;
  }
  .squares-anim{
    position: absolute;
    height: 30%;
    right: 0;
    bottom: 0;
    animation: mover 2s infinite  alternate;
  }
  @keyframes mover {
    0% { transform: translateY(10px); }
    100% { transform: translateY(-10px); }
  }


  #aboutUs{
    background-image: url(../assets/nosotros.png);
    color: #fff;
  }
  .section-format{
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;
    width: 100%;
    min-height: 100%;
    display:flex;
    flex: 1 1 100%;
  }
  #aboutUs .contain{
    padding: 10% 10% 0px;
  }
  #aboutUs #title{
    font-size: 31px;
    font-weight: 400;
    letter-spacing: 4px;
    height:78px;
  }
  #aboutUs .body{
    font-size: 20px;
    letter-spacing: 2px;
    font-weight: 400;
  }
  #aboutUs .squares-anim{
    height:38%;
    position: absolute;
    left: 0;
    bottom: 0;
    animation: mover 2s infinite  alternate;

  }
  @media only screen and (max-width: 1696px){
    .section-format{
      min-height:85%;
    }
    #aboutUs .contain{
      padding: 10% 0px;
    }
  }
  @media only screen and (max-width: 1440px){
    .squares-anim{
      height:300px;
    }
    #aboutUs .squares-anim{
      height:380px;
    }
  }
  @media only screen and (max-width: 1024px){

    #aboutUs .contain{
      padding: 0px;
    }
    .squares-anim{
      height:150px;
    }
    #aboutUs .squares-anim{
      height:180px;
    }
  }
  @media only screen and (max-width: 900px){
    .section-format{
      max-height:700px;
      min-height:5%;
    }
  }
  @media only screen and (max-width: 768px){

    .section-format{
      height:1200px;
    }
  }

</style>
