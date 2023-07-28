<template>
    <div>
        <p>{{ compEmail }}</p>
        <p v v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades!</p>
        <p>Utilizo as seguintes tecnologias para back-end:</p>
        <ul>
                <li v-for="(tecnology, index) in backend_tecnologies" v-bind:key="index">{{ tecnology }}</li>         
        </ul>  
        <p>Utilizo as seguintes tecnologias para front-end:</p> 
        <ul>
                <li v-for="technology in frontend_tecnologies" :key="technology.id"> 
                    {{ technology.language }}
                </li>         
        </ul> 
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}.</p>
        <p class="teste">Para acessar meu portfólio <a v-bind:href ="meu_link" target="_blank">basta clicar aqui</a></p>
        <p v-if=" 4 > 2">Testando.</p>    
        <Picture />
    </div>  
</template>

<script>
import Picture from './Picture.vue';

export default {
    name: 'Information',
    components: {
        Picture
    },
    data() {
        return {
            esta_trabalhando: false,
            mostrar_email: false,
            email: 'alex@google.com',
            meu_link: 'https://google.com',
            textoBotao: 'Mostrar E-mail',
            backend_tecnologies: ['JavaScript', 'PHP', 'Python'],
            frontend_tecnologies: [
                {id:1, language: 'HTML'},
                {id:2, language: 'CSS'},
                {id:3, language: 'VUE'}
            ]
        }
    },
    methods: {
        showEmail() {
            this.mostrar_email = !this.mostrar_email

            if(!this.mostrar_email) {
                this.textoBotao = 'Mostrar E-mail'
            }
            else {
                this.textoBotao = 'Esconder E-mail'
            }
        }
    },
    props: {
        compEmail: String
    }
}
</script>