<template>
    <div>
        <p>Olá {{nome}}</p>
        {{dia}}
        <v-btn color="blue" height="100" @click="trocarNome('vitor')">Trocar nome</v-btn>
    </div>
</template>

<script>
export default {
    data: () => ({
        nome: 'Rafinha'
    }), 
    methods: {
        trocarNome(nome){
            this.nome = this.definirNome(nome)
        },
        definirNome(nome){
            return nome;
        }
    },
    computed:{
        dia(){
            return 3

        }
    },
    watch:{
        nome(newvalue, velho){
            console.log(newvalue)
            console.log(velho)
        }
    },
    created(){
        this.nome = "Joao"
    }

}
</script>

<style>

</style>