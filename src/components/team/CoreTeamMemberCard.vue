<template>
    <v-dialog
      v-model="dialog"
      width="700"
    >
      <template v-slot:activator="{ on }">
          <div v-on="on" style="cursor: pointer;" class="text-center py-5 ma-1 fill-height" :class="$vuetify.theme.dark == true?'darkModeCard':'whiteTheme'" >
               <v-avatar size="100">
                  <img 
                    :src="getImgUrl(data.image, 'profile.jpg')"
                    :lazy-src="getImgUrl(data.image, 'profile.jpg')" alt=""
                  >
                </v-avatar>
                <p class="mt-3 mb-0 google-font mb-0" style="font-size:120%">PRINCIPALES OBJETIVOS</p>
                <p class="mt-1 mb-0 google-font mt-0" style="font-size:80%">Seguidad</p>

                
                <socialMediaDetails :data="data.socialLinks"/>
          </div>
          
      </template>

      <v-card :class="theme.isDark?'grey darken-3':'white'">
        <v-card-title
          class="px-5 google-font"
          primary-title
        >
     La seguridad IA en negocios 
        </v-card-title>

        <v-card-text class="pa-5">
            <p class="google-font">seguridad de inteligencia artificial>
            <p class="google-font">Con la seguridad de inteligencia artificial,
               las cámaras y otros equipos básicamente hacen mucho del 'trabajo pesado'
                de seguridad, lo que quita mucha presión de los negocios  Al mismo tiempo,
                 la seguridad de la IA ayuda a minimizar sus falsas alarmas, lo que reduce 
                 los costos y ahorra aún más tiempo.</p>
            
            <socialMediaDetails  class="pl-0 ml-0" :data="data.socialLinks"/>

            <v-btn class="primary mt-3" small depressed @click="goToTeam(data.id)">Click para mas informacion</v-btn>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="primary"
            text
            @click="dialog = false"
          >
            cerrar
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
</template>

<script>
import socialMediaDetails from '@/components/common/SocialInfo'
  export default {
    components:{
        socialMediaDetails
    },
    inject: ['theme'],
    props:['data'],
    data () {
      return {
        dialog: false,
      }
    },
    mounted(){
     
    },
    methods:{
      goToTeam(id){
        this.$router.push("/team/" + id);
      },
    },
    filters:{
        summery: (val,num)=>{
          if(val.length > num)
            return val.substring(0,num)+".."
          else
            return val;
        }
    }
  }
</script>

