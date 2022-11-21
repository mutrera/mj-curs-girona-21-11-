<template>
    <v-container>
     <v-row>
        <!--  v-if="!enviat -> si no s'ha enviat o  v-if="enviat == false" -->
        <v-col cols="6" v-if="!enviat">
         <v-text-field
        label="Nom i cognoms"
        v-model="nomComplet">
        </v-text-field>
<v-text-field
    label="Correu electrònic" 
    type="email"
    v-model="correuElectronic">
</v-text-field>

    <v-checkbox 
    label="Accepta la política de privacitat"
    v-model="politicaPrivacitat">

    </v-checkbox>

    <v-btn @click="enviar()">enviar</v-btn>
    <v-btn @click="netejar()">netejar</v-btn>

</v-col>
<v-col cosl="6" v-else>
    <h1>Missatge enviat</h1>
</v-col>
<v-col cols="6">
    {{nomComplet}}
    <br>
    {{correuElectronic}}
    <br>
    {{politicaPrivacitat}}
</v-col>
</v-row>
</v-container>
</template>

<script>
export default{
    mounted(){
    this.nomComplet ="Jordi",
    this.correuElectronic ="jordi@google.com"
    this.politicaPrivacitat= true

},
    data(){
        return{
            nomComplet:"",
            correuElectronic:"",
            politicaPrivacitat:false,
            enviat:false
        }
    },
    methods:{
        netejar(){
            this.nomComplet=""
            this.correuElectronic=""
            this.politicaPrivacitat=false
        }, 
        enviar(){
            if(this.politicaPrivacitat== true){
            console.log("estic canviant...")
            console.log(this.nomComplet)
            console.log(this.correuElectronic)
            console.log(this.politicaPrivacitat)
            this.enviat = true
        }

        }
    }

}
       
    </script>