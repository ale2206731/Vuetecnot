<template>
    <v-container fluid class="py-0 my-0 mt-5">
        <!-- <v-row class="py-0 my-0">
            <v-col md="12" sm="12" cols="12" class="py-0 my-0">
                
            </v-col>
        </v-row> -->
        <v-row align="center" class="py-0 my-0 mb-5">
            <v-col md="8" sm="12" cols="12" class="py-0 my-0">
                <h1 class="google-font mb-2">Donde y en que se utiliza las IA de los negocios</h1>
                <!-- {{communitydata.CommunityGuideline}} -->
                <v-expansion-panels accordion>
                    <v-expansion-panel
                      
                        
                    >
                        <v-expansion-panel-header style="font-size:110%;color: #0ED305;">Cómo se integra la Inteligencia Artificial en el mundo de los negocios</v-expansion-panel-header>
                        <v-expansion-panel-content>
                            la IA ofrece enormes ventajas sobre la automatización tradicional, ya sea agilizando la cadena de producción, facilitando 
                            la gestión de la cadena de suministro o simplificando el proceso de venta.
                            Al acelerar el desarrollo de nuevos productos, la Inteligencia Artificial ayuda a potenciar la innovación, eliminar
                             los costos repetidos y generar nuevos flujos de ingresos para aumentar la rentabilidad
                        </v-expansion-panel-content>
                        <v-expansion-panel-header style="font-size:110%;color: #0ED305;">Sectores que utilizan la Inteligencia Artificial</v-expansion-panel-header>
                        <v-expansion-panel-content>
                            En los negocios, la Inteligencia Artificial puede usarse como aliada en ventas, o para mejorar la productividad o 
                            los procesos operativos Entre los sectores más beneficiados se encuentran el área de marketing, que ha sabido aprovechar 
                            las ventajas de esta tecnología para crear experiencias personalizadas.
                        </v-expansion-panel-content>
                        <v-expansion-panel-header style="font-size:110%;color: #0ED305;">¿Que ventajas tiene la Inteligencia Artificial en el mundo de los negocios?</v-expansion-panel-header>
                        <v-expansion-panel-content>
                            Aplicando esta tecnología les es posible incrementar la productividad y eficiencia, así como mejorar la experiencia del cliente, 
                            identificando preferencias,
                             diseñando contenidos exclusivos y orientándolos a las personas con mayores posibilidades de generar una interacción correcta.
                        </v-expansion-panel-content>
                    </v-expansion-panel>
                </v-expansion-panels>
            </v-col>
            <v-col md="4" sm="4" cols="12" class="py-0 my-0 hidden-sm-and-down">
                <v-img
                    :src="require('@/assets/img/svg/bg.svg')"
                    :lazy-src="require('@/assets/img/svg/bg.svg')"
                    width="60%"
                    style="float:right"
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