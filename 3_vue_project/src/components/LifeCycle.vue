<template>
    <h1>Meu nome é: {{ nome }}.</h1>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return{
            nome: 'Sei lá!!'
        }
    },
    created() {
        setTimeout(() => {
            this.nome = 'Matias'
        }, 2000);
        this.lifecycle()
    },
    mounted() {
        setTimeout(() => {
            this.nome = 'Pedro'
        }, 1000);
        this.lifecycle()
    },
    methods: {
        lifecycle() {
            console.log("Executou..")
        }
    }    
}
</script>