<template>
    <div class="net-card" v-bind:style="efeitoClick" v-on:click="clickEfeito()" v-on:mouseout="removeClickEfeito">
        <div class="net-card__media">
            <img class="net-card__img" v-bind:src="imagem" alt=""  />
        </div>
        <div class="net-card__details">
            <div class="net-card__title">
            {{titulo}}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:['titulo','imagem'],
    data(){
        return{
            efeitoClick: null
        }
    },
    methods: {
        clickEfeito: function() {
            this.efeitoClick = 'transform: scale(1.9); margin-right: 10%';
        },
        removeClickEfeito: function() {
            this.efeitoClick = null;
        }
    }

    
}
</script>

<style lang="scss">
    
</style>