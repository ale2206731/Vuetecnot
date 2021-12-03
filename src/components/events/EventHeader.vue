<template>
    <v-container fluid class="py-0">
        <v-row align="center">
            <v-col md="12" sm="12" cols="12">
                <p class="google-font mb-0" style="font-weight: 350;font-size:200%;color: #2AFF00;"><b>
                    ¿Que es la infraestructura 
                    <span style="color: #002BFF;">IA?</span> </b> 
                </p>
                <p  class="google-font mt-0 mb-0" style="font-size:110%">Es una disciplina dentro de la

                     informática y la ingeniería cuyo objetivo es el desarrollo de sistemas  
                     <a style="color:#1565C0;text-decoration: none;" :href="`mailto:${config.generalConfig.email}`"></a></p>
                     <p>inteligentes 
                     capaces de aprender y adaptarse tomando como referencia la inteligencia humana.</p>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import { mapState } from "vuex";
export default {
    data() {
        return {
        }
    },
    computed:{
        ...mapState(["config"])
    },
}
</script>