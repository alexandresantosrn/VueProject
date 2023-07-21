<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}.</h2>  
        <Information />               
    </div>   
</template>

<script>
import Information from './Information.vue';

export default {
    name: 'Pessoa',
    components: {
        Information
    },
    data() {
        return {
            nome: 'Alexandre'
        }
    }
}
</script>