<template>
    <v-container fluid class="py-0">
        <v-row align="center">
            <v-col md="12" sm="12" cols="12">
                <p class="google-font mb-0" style="font-weight: 350;font-size:200%;color:#3CFF33;"><b>INFRAESTRUCTURA DE LOS

                    <span style="color: #3CFF33;">NEGOCIOS  (IA) </span> </b> 
                </p>
                <p class="google-font mt-0 mb-0" style="font-size:110%">Tiene una gran importancia en el mundo de los negocios la IA  <a style="color:#1565C0;text-decoration: none;" :href="`mailto:${config.generalConfig.email}`"></a></p>
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