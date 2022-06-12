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

      <v-toolbar-title> <v-toolbar-tittle style="text-transform:uppercase; margin-top: 5px; font-size: 35px; font-family: Georgia, 'Times New Roman', Times, serif;" >FEELINGS</v-toolbar-tittle></v-toolbar-title>
      
      

      
      <v-spacer></v-spacer>

      


      
      <v-divider vertical></v-divider>

    

      <v-divider vertical></v-divider>


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
                to=""><H2>FEELINGS</H2></v-btn>
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







  <v-footer app color="black" padless>
    <!-- -->
    <v-row
      justify="center"
      no-gutters
    >
      <v-col
        class="text-center white--text"
        cols="20"
      >
         <strong>UNIVERSIDAD DE CÓRDOBA</strong>-{{ new Date().getFullYear() }}
         
      </v-col>
    </v-row>
  </v-footer>
</v-app>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgb(245, 250, 255);
}
 
nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #f7fbff;
}

nav a.router-link-exact-active {
  color: #6c1ec6;
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
