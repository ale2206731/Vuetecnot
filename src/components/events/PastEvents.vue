
<template>
    <v-container fluid>
        <v-snackbar v-model="errorAlert" bottom left>
            {{ errorMsg }}
            <v-btn color="pink" text @click="errorAlert = false">Close</v-btn>
        </v-snackbar>
        <v-row align="center" justify="center" class="mb-5">
            <v-col cols="12" md="12" lg="12" sm="12" class="">
                <v-row>
                    <v-col md="6" lg="6" sm="6" cols="12">
                        <p class="google-font mb-0" style="font-size:200%;color: #3CFF33;">Benefios de las IA En los negocios</p>
                        <p class="google-font mt-0 mb-0" > <b style="font-size:95%;color: #FFA233;">1.-Sistemas inteligentes:</b> 
                        Tiene que ver con emplear el aprendizaje automático para crear sistemas inteligentes 
                        que sean capaces de tener niveles de interacción casi humanos.</p>

                        <p class="google-font mt-0 mb-0" > <b style="font-size:95%;color: #FFA233;">2.-Analítica del Big Data:</b> 
                        Acceso a las herramientas que necesita para extraer conocimientos valiosos
                        de grandes cantidades de datos no estructurados. Estas, sirven a los líderes empresariales tomar
                         decisiones inteligentes y rápidas basándose en el enorme mar de datos que gestionan, identificar 
                         nuevas fuentes de ingresos, a mejorar las experiencias de los clientes y a reducir los costos.</p>

                         <p class="google-font mt-0 mb-0" > <b style="font-size:95%;color: #FFA233;">3.- Cloud:</b> 
                        No hay que elegir entre agilidad, tiempo de comercialización o eficiencia operativa.</p>

                        <p class="google-font mt-0 mb-0" > <b style="font-size:95%;color: #FFA233;">4.-Data Science:</b> 
                     Asegura tus modelos, información y resultados en tus propios servidores y 
                      personalízalos para tu compañía: explora y aprende, modela y evalúa, desarrolla y predice, monitorea y 
                      mide.</p>

                      <p class="google-font mt-0 mb-0" > <b style="font-size:95%;color: #FFA233;">5.- El software y los algoritmos adecuados:</b> 
                      IBM cuenta con el software que le ayudará a entrenar, implementar
                      y optimizar en miles de núcleos, desde la optimización de núcleos y la gestión de cargas de trabajo hasta 
                      las infraestructuras de aprendizaje profundo de código abierto,</p>


                        
                    </v-col>
                </v-row>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import service from '@/services/appservices'
import { mapState } from 'vuex'
    export default {
        name: 'App',
        components:{
        },
        computed:{
            ...mapState(["config"])
        },
        data: () => ({
            eventsData:[],
            showData: false,
            isLoading: true,
            search:'',
            notFoundUpcomingEventFlag: false,
            errorAlert: false,
            errorMsg: '',
            headers: [
                {
                    text: 'Event Name',
                    align: 'start',
                    value: 'name',
                },
                { text: 'Date', value: 'local_date' },
                { text: 'See More', value: 'link' },
            ],
        }),
        mounted(){
            this.getAllMeetupPastEvents()
        },
        methods:{
            getAllMeetupPastEvents(){
                this.isLoading = true
                service.getAllMeetupPastEvents(this.config.keysandsecurity.meetup).then(res=>{
                    if(res.success){
                        this.eventsData = res.data
                        this.isLoading = false
                    }else{
                        this.isLoading = false
                    }
                }).catch(e=>{
                    this.errorMsg = "Issue found with " + e;
                    this.isLoading = false
                    this.errorAlert = true;
                })
            }
        }
    };
</script>