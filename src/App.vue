<template>
  <v-app>
    <v-app-bar app dense color="black">
      <v-spacer></v-spacer>
      <v-toolbar-title class="white--text text-sm-h4">VICAM</v-toolbar-title>
       <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <v-img src="./assets/jungle.png" height="100%">
      <v-container id="container">
        
        <v-layout wrap justify-center align-center style="height:500px">
          
          <v-flex xs9 sm9 md3 l3 xl3 mx-5 my-4>
            <v-expand-transition>
              <v-card v-show="expand" height="490" width="auto" class="rounded-xl" color="grey lighten-5">

                <v-img
                src="./assets/img1.jpeg"
                height="240px">
                </v-img>

                <v-card-title>
                  Misión
                </v-card-title>
              
                <v-card-text>
                Somos una empresa dedicada a la producción y exportación de frutas de calidad.
                </v-card-text>

              </v-card>
            </v-expand-transition>

          </v-flex>

          <v-flex xs9 sm9 md3 l3 xl3 mx-5 my-4>
            <v-expand-transition>
              <v-card v-show="expand" height="490" class="rounded-xl" color="grey lighten-5">
                <v-img
                src="./assets/img2.jpeg"
                height="240px">
                </v-img>

                <v-card-title>
                  Visión
                </v-card-title>

                <v-card-text>
                Ser líderes en la producción y exportación de frutas de calidad, movernos hacia un crecimiento rentable y hacer de <strong>VICAM</strong> mejor para servir a nuestro clientes.
                </v-card-text>
              </v-card>
            </v-expand-transition>
          </v-flex>

          <v-flex xs9 sm9 md3 l3 xl3 mx-5 my-4>
            <v-expand-transition>
              <v-card v-show="expand" height="490" width="1000" class="rounded-xl" color="grey lighten-5">
                <v-img
                src="./assets/img3.jpg"
                height="240px">
                </v-img>

                <v-card-title>
                  Valores
                </v-card-title>

                <v-card-subtitle>
                  <strong>Compromiso, calidad, responsabilidad social</strong>
                </v-card-subtitle>

                <v-card-text>
                "Al actuar de acuerdo con estos valores, inspiraremos la lealtad de nuestros clientes, obtendremos una posición de liderazgo y proporcionaremos un rendimiento superior a nuestros accionistas."
                </v-card-text>
              </v-card>
            </v-expand-transition>
          </v-flex>

        </v-layout>
      </v-container>
      </v-img>
    </v-main>

    <v-footer color="black" v-show="expand">
      <v-slide-x-transition>
        <v-card v-show="expand" color="black" width="100%" height="auto">
          <v-card-text class="white--text text-center" mt-0>
            &copy; VICAM 2021
            <br>
            Desarrollado por Martín Camacho. 
          </v-card-text>
          <v-card-text class="text-center">
            <v-btn v-for="icon in icons" :key=icon class="white--text mx-4" icon>
              <v-icon size="24px">
                {{ icon }}
              </v-icon>
            </v-btn>
          </v-card-text>
        </v-card>
      </v-slide-x-transition>
    </v-footer>
  </v-app>
</template>

<script>


export default {
  name: 'App',

  components: {
  },

  data: () => ({
    icons: [        
      'mdi-facebook',
      'mdi-twitter',
      'mdi-instagram'
    ],
    expand: false
  }),
  mounted(){
    this.expand = true;
  }
};
</script>

<style>
#container{
  overflow-y: scroll;
}
html{
  overflow: hidden;
}
::-webkit-scrollbar {
    width: 6px;
    height: auto;
}
::-webkit-scrollbar-thumb {
  -webkit-border-radius: 6px;
  border-radius: 6px;
  background: black;
}
</style>

