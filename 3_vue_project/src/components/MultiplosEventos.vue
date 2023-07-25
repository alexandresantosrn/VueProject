<template>
    <div>
        <button @click="primeiro($event), segundo(txt2, $event)">Ativar Múltiplos Eventos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>

<script>
export default {
    name: 'MultiplosEventos',
    data() {
        return {
            multiplos_eventos: "",
            txt2: "Segundo evento ativado!"
        }
    },
    methods: {
        primeiro(e) {
            this.multiplos_eventos = "Primeiro evento ativado!"
        },
        segundo(txt2) {
            setTimeout(() => this.multiplos_eventos = txt2, 1000)
        }
    }
}
</script>

<style scoped>
div {
    margin: 100px;
}
</style>