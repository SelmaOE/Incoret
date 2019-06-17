<template>
  <v-app>
    <div id="firstSection" class="section-format">
      <v-container fluid fill-height>
        <v-layout row align-center>
          <div class="my-flex">
            <v-flex offset-xs2>
              <hr class="hr-left">
            </v-flex>
            <v-flex offset-xs2>
              <h1 id="title" class="fade-anim">INCORET</h1>
            </v-flex>
            <v-flex xs5>
              <hr class="hr-right">
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
          <v-flex offset-(xs1|sm3 mt-4 mr-5)>
            <h2 id="title" class="text-xs-center py-3"
            :class="{'title-anim': animation}">NOSOTROS</h2>
            <hr v-observe-visibility="visibilityChanged"
                    :class="{'hr-right': animation}">
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
    data(){
        return {
            animation:false
        }
    },
    methods:{
        visibilityChanged(isVisible){
            console.log(isVisible)
            if(isVisible)
                this.animation = true;
        }
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

  .hr-left{
    animation: floatLeft 1s 1;
  }
  @keyframes floatLeft{
    0%{transform:translateX(1200px);}
    to{transform:translateX(0);}
  }

  .hr-right{
    animation: floatRight 1s 1;
  }
  @keyframes floatRight{
    0%{transform:translateX(-1200px);}
    to{transform:translateX(0);}
  }

  .fade-anim{
    animation: fade-title 3s 1;

  }
  @keyframes fade-title{
    0%{opacity:0}
    to{opacity:1}
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
    min-height: 130%;
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
  @media only screen and (max-width: 1400px){
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
  }
  @media only screen and (max-width: 600px){
    #firstSection{
      background-size:cover;
    }
    .section-format{
      background-size: auto;
      min-height: 60%;
    }
  }
  @media only screen and (max-width: 432px){
    .section-format{
      min-height: 85%;
    }
    #aboutUs{
    background-position-x: -600px
    }
  }

</style>
