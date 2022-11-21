<template>
    <!--fem una prova 
        <div>
        hola camp de text
    </div> -->
   <div>
    <!-- <v-text-field 
    :label="text"
    placeholder="p.e Sandra"
    >
    </v-text-field>
    <v-text-field 
    label="Escriu el teu nom"
    solo>
    </v-text-field>
    <v-text-field 
    label="Escriu el teu nom"
    outlined>
    </v-text-field>
    <v-text-field 
    label="Escriu el teu nom"
    filled>
    </v-text-field> -->
    <v-text-field 
    label="Escriu el teu nom"
    v-model="nom">
    </v-text-field> 
    <v-btn @click="emplenar()">Emplenar</v-btn>
    <v-btn @click="enviar()">Enviar</v-btn>
 </div> 
</template>
<script>
export default{
    data(){
        return{
            nom:""
        }
    },
    methods:{
        enviar(){
            console.log("enviat,")
        }
    },
    methods:{
        emplenar(){
            this.nom ="Sandra"
        }
    },
}
</script>