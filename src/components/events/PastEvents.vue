
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
                        <p class="google-font mb-0" style="font-size:150%;color: #2AFF00;">Benefios de IA en negocios</p>
                        <p class="google-font mt-0 mb-0" style="font-size:95%"> <b> 1.- Sistemas inteligentes:</b> 
                        Tiene que ver con emplear el aprendizaje automático para crear sistemas inteligentes que sean capaces de tener niveles de interacción casi humanos.</p>
                       <b></b> 
                        <p class="google-font mt-0 mb-0" style="font-size:95%"> <b> 2.- Analítica del Big Data:</b> 
                        Tiene que ver con emplear el aprendizaje automático para crear sistemas inteligentes que sean capaces de tener niveles de interacción casi humanos.</p>

                        <p class="google-font mt-0 mb-0" style="font-size:95%"> <b> 3.-  Cloud:</b> 
                        No hay que elegir entre agilidad, tiempo de comercialización o eficiencia operativa.</p>
                    
                    <p class="google-font mt-0 mb-0" style="font-size:95%"> <b> 4.-El software y los algoritmos adecuados:</b> 
                        IBM cuenta con el software que le ayudará a entrenar, implementar y optimizar en miles de núcleos, desde la
                        optimización de núcleos y la gestión de cargas de trabajo hasta las infraestructuras de aprendizaje profundo de código abierto</p>
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