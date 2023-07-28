<template>
    <button @click="$emit('mudarImagem')">Trocar imagem do perfil</button>
</template>

<script>
export default {
    name: 'MudarImagem',
    emits: ['mudarImagem']
}
</script>