<template>
<!-- App.vue -->
<v-app>

    <v-app-bar
      app
      class="text-center white--text"
      color="gray"
      dark
      src="../assets/banner.jpg" 
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title><h2> UNIVERSIDAD DE CÓRDOBA</h2></v-toolbar-title>
      

      
      <v-spacer></v-spacer>

      

    <v-toolbar-items class="hidden-sm-and-down" >
      
      <v-divider vertical></v-divider>

      
      <v-btn 
      class="text white--text"
        text
        to="/contenidos"> <h3>Contenidos</h3></v-btn>

      <v-divider vertical></v-divider>

      <v-btn 
      class="text white--text"
       text
       to="/actividades"><h3>Actividades</h3></v-btn>


      <v-divider vertical></v-divider>

      <v-btn 
      class="text white--text"
        text
        to="/evaluacion"><h3>Evaluación</h3></v-btn>
              <v-btn 
        class="text white--text"      
        text
        to="/Creditos"><h3>Creditos</h3></v-btn>

      <v-divider vertical></v-divider>
    </v-toolbar-items>

<v-divider vertical></v-divider>
<v-spacer></v-spacer>
      <v-btn class="back" to="/contenidos" icon>
        <v-icon >mdi-home</v-icon>
      </v-btn>
      <v-btn class="back" to="" icon>
        <v-icon>mdi-export</v-icon>
      </v-btn>

    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      bottom
      temporary
      color="blue"
      src="../assets/fondo.jpeg"
    >
    
      <v-list
        nav
        dense
        dark
        
      >
        <v-list-item-group
          v-model="group"
          active-class="text white--text"
        >
        

               <v-list-item>
              <v-btn 
              class="text white--text"
                block
                text
                to=""><H2>VARIABLES</H2></v-btn>
          </v-list-item>

          <v-list-item>
            <v-icon>mdi-format-list-checks</v-icon>
              <v-btn 
              class="text white--text"
                block
                text
                to="/contenidos">Contenidos</v-btn>
                
          </v-list-item>

          <v-list-item>
            <v-icon>mdi-format-list-checks</v-icon>
              <v-btn 
              class="text white--text"
                block
                text
                to="/actividades">Actividades</v-btn>
          </v-list-item>

          <v-list-item>
            <v-icon>mdi-format-list-checks</v-icon>
              <v-btn 
              class="text white--text"
                block
                text
                to="/evaluacion">Evaluacion</v-btn>
            
          </v-list-item>

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
               <v-list-item>
                  <v-icon>mdi-run-fast</v-icon>
              <v-btn 
             
              class="text white--text"
                block
                text
                to="/creditos">Creditos</v-btn>
          </v-list-item>

        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>



  <!-- Sizes your content based upon application components -->
  <v-main>
      
    <!-- Provides the application the proper gutter -->
    <v-container fluid>
        <router-view></router-view>
      <!-- If using vue-router -->
      <slot></slot>
    </v-container>
  </v-main>

    <v-spacer></v-spacer>
 
<v-toolbar-tittle style="text-transform:uppercase; margin-top: 5px; font-size: 35px; font-family: Georgia, 'Times New Roman', Times, serif;" >INTEGRANTES</v-toolbar-tittle>
  <br>
    <v-spacer></v-spacer>

    <v-row>
        

        <v-col>
              <center><font color="white"> <h4>Jesus David Valdelamar Vega.</h4></font>
                <v-img class="fotos" src="../assets/imagenes/jesus.png"></v-img></center>
        </v-col>

        <v-col>
              <center><font color="white"> <h4>Jaider Martinez Paternina.</h4></font>
                <v-img class="fotos" src="../assets/imagenes/jaider.jpeg"></v-img></center>
        </v-col>

        <v-col>
              <center><font color="white"> <h4>Mayerlis Bruno Aguirre.</h4></font>
                <v-img class="fotos" src="../assets/imagenes/maye.jpg"></v-img></center>
        </v-col>

        <v-col>
              <center><font color="white"> <h4>Maria Camila Salgado Montiel.</h4></font>
                <v-img class="fotos" src="../assets/imagenes/maria.jpeg"></v-img></center>
        </v-col>

    </v-row>

    <v-row>
        
            <v-spacer></v-spacer>
            <br>
            <v-toolbar-tittle style="text-transform:uppercase; margin-top: 5px; font-size: 35px; font-family: Georgia, 'Times New Roman', Times, serif;" >DOCENTE</v-toolbar-tittle>
            <br>
            <br>
            <v-spacer></v-spacer>
        
    </v-row>
<v-col>
  <center>
    <font color="white"> <h4>Aly Culchac de la vega</h4></font>
    <v-img class="fotos" src="../assets/imagenes/Aly.jpeg"></v-img>
    </center>
</v-col>
</v-app>
</template>


<style>
#app {
  font-family: Avenir, Helvetica,'Times New Roman', Times, serif, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-image: url("../assets/creditos\ 2.jpg");
  color: #f0f8fe;
}
 
nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #6c1ec6;
}

.fotos{
    width: 150px;
    display: block;
    margin: 10 auto 0;
}

</style>

<script>


export default {
    name: 'PaginaView',

        data: () => ({
      drawer: false,
      group: null,

    }),

    methods:  {
      goContent() {
         
    },
    },

    watch: {
      group () {
        this.drawer = false
      },
    },

    
}
</script>
