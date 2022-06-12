<template>
<!-- App.vue -->

<v-app>
  <!-- Sizes your content based upon application components -->
  <v-main class="fondo">

    <!-- Provides the application the proper gutter -->
    <v-container>
    <br><br>
    <br><br>
    <br><br>
    <v-row no-gutters>
      <v-col align="center">
        <input type="button"/>
        <div class="content fondo2 imagen" >
          <router-link :to="{ name: 'contenidos' }" class="text-decoration-none routernone" >
            <v-img class="play " src="../assets/logo.png"></v-img> 
            <v-img class="play " src="../assets/texto.png"></v-img> 
          </router-link>
          <div class="sombra"></div>

        </div>
      </v-col>
    </v-row>
  
  </v-container>
  </v-main>


</v-app>


</template>

<style>

        .fondo{
          background-image: url(../assets/background.png); 
                  
        }
          .title{
            color: rgb(229, 229, 229);
            
            
          }
        .content{
            width: 100%;
            height: 90%;
        }

        .play{
            width: 410px;
            left: 410px;
            background-size: cover;
            animation: animar  1s infinite alternate;
            }

        .sombra{
            height: 400px;
            width: 400px;
            background:rgb(90, 211, 193);
            border-radius: 100%;
            transform: rotatex(-90deg);
            animation: sombra 2s infinite alternate;
        }
        @keyframes animar{
            to{
                transform: translateY(-50px)
            } 
        }

        @keyframes sombra{
            to{
                transform: scale(0.6) rotateX(-70deg);
                opacity: 0.2;
            }
        }
      
</style>


<script>
export default {
  name: "PantallaEntrada",
  data: () => ({

  }),

  beforeDestroy() {
    },
};
</script>