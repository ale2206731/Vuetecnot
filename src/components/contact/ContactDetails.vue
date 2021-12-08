<template>
  <v-container fluid class="py-0 my-0 mt-0">
    <v-row class="py-0 my-0">
      <v-col md="9" sm="6" cols="12" class="py-0 my-0">
        <p
          class="google-font mb-1"
          style="font-size:110%"
        >En esta pagina desarrollamos diferentes ventas para todo la 
        informacion nesesaria que deseas saber </p>
        <p class="google-font">Trabajamos en esta pagina para poder dar a conocer 
          todos y cada unis de los apartados sobre la inteligencia articial en los
        </p>
        <p class="google-font mt-5 style=color:#1a73e8;"> puedes buscarnos en nuestras diferentes redes sociales</p>
        
        <CommunitySocialInfo :config="config"  class="mb-2"/>
        <span v-for="(item,i) in data.hashtags" :key="i" >
          <v-chip
            class="mr-1 mb-1"
            :href="'https://twitter.com/hashtag/'+Yaz & Alex"
            target="_blank"
            label
          >#Yaz & Alex</v-chip>
        </span>
      </v-col>
      <v-col md="3" sm="6" cols="12" class="py-0 my-0">
        
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
// import SocialInfo from '@/components/common/SocialInfo'
import { mapState } from 'vuex'

export default {
  components:{
      CommunitySocialInfo : ()=>import('@/components/common/CommunitySocialInfo'),
    },
    data:()=>({
    }),
    computed:{
      ...mapState(['config'])
    },
  props: ["data"],
};
</script>