<template>
    <v-container>
        <v-row>
            <v-col cols="6" class="coldreta">
             <v-text-field 
                 label="Número 1"
                 type="number"
                 v-model="numero1">
             </v-text-field>
             <v-text-field 
                label=" Número 2"
                type="number"
                v-model="numero2">

             </v-text-field>
             <v-btn @click="sumar()">+</v-btn>
             <v-btn @click="restar()">-</v-btn>
             <v-btn @click="multiplicar()">*</v-btn>
             <v-btn @click="dividir()">/</v-btn> 
             <br>
            <br>  
             <v-btn @click="netejat()">netejar</v-btn> 
            </v-col>

            <v-col cols="6" class="colesquerra">
                <h2>Resultat</h2>
                {{resultat}}
                <br>
                <br>
                <br>
                

            </v-col>
        </v-row>
    </v-container>
</template>
<script>
export default{
    data(){
        return{
            numero1:0,
            numero2:0,
            resultat:0
        }      
    },  
    
    methods:{
        sumar(){
            var a = parseFloat(this.numero1)
            var b = parseFloat(this.numero2)
            this.resultat=a+b
        },
        restar(){
            var a = parseFloat(this.numero1)
            var b = parseFloat(this.numero2)
            this.resultat=a-b

        },
       multiplicar(){
            var a = parseFloat(this.numero1)
            var b = parseFloat(this.numero2)
            this.resultat=a*b

       },
       dividir(){
            var a = parseFloat(this.numero1)
            var b = parseFloat(this.numero2)
            this.resultat=a/b

       },
       netejat(){
            this.numero1 = 0  
            this.numero2 = 0
            this.resultat= 0

       } 
       
      
    

    }
}

</script>
<style>
h1{
    background-color:cornflowerblue;

}
.coldreta{
    border:5px solid  rgb(173, 156, 170);
}
.colesquerra{
    border:5px solid  rgb(240, 209, 164);
}
</style>