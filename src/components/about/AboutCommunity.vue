<template>
    <v-container fluid class="py-0 my-0 mt-2 mb-5">
        <v-row class="py-0 my-0" align="center">
            <v-col md="4" sm="12" cols="12" class="py-0 my-0">
                <v-img
                    :src="require('@/assets/img/dontremove/about.png')"
                    :lazy-src="require('@/assets/img/dontremove/about.png')"
                    class=" mb-3"
                    width="100%"
                >
                    <template v-slot:placeholder>
                        <v-row
                        class="fill-height ma-0"
                        align="center"
                        justify="center"
                        >
                        <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                        </v-row>
                    </template>
                </v-img>
            </v-col>
            <v-col md="8" sm="12" cols="12" class="py-0 my-0">
                <!-- {{data}} -->
                <p class="google-font mt-0" style="font-size:110%"> aplicación 
                    de Inteligencia Artificial en las empresas, es verdad que la Inteligencia Artificial en el
                     mundo de los negocios continúa teniendo avances significativos año con año. Cada vez más
                      empresas se suman a la transformación integrando soluciones que les aportan grandes beneficios
                       y les ayudan a generar mayores ingresos, al tiempo que mejoran su productividad.
                       gracias al uso de aplicaciones basadas en Inteligencia Artificial es posible generar mejores 
                       experiencias de usuario, mejor la atención al cliente, recopilar y analizar datos, crear 
                       productos personalizados y mucho más.</p>
                <br>
                <v-btn v-if="checkExistance(data.becomemember, 0)" :href="data.becomemember" target="_blank" class="ma-0 google-font elevation-1 primary" style="text-transform: capitalize;border-radius:5px;color:white">Conocer mas </v-btn>

                &nbsp;

                <v-btn v-if="checkExistance(data.learnMoreLink, 0)" :href="data.learnMoreLink" target="_blank" rounded color="cyan" style="text-transform: capitalize;border-radius:5px;text-transform: capitalize;" outlined  class="ml-0" dark>segir leyendo</v-btn>

            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    props:['data'],
    data:()=>({

    })
}
</script>