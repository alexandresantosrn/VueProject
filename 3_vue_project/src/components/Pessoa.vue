<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}.</h2>  
        <Information :compEmail="compEmail" />    
        <Form />           
    </div>   
</template>

<script>
import Information from './Information.vue';
import Form from './Form.vue';

export default {
    name: 'Pessoa',
    components: {
        Information,
        Form
    },
    data() {
        return {
            nome: 'Alexandre',
            compEmail: 'matias@hotmail.com'
        }
    }
}
</script>