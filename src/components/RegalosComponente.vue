<template>
    <div class="row">
        <CartaRegalo v-for="(regalo,index) of regalos" :key="index" :regalo="regalo"/>
    </div>
</template>

<script>
import CartaRegalo from './CartaRegalo.vue';

export default {
    name: 'RegalosComponente',
    data() {
        return {
            regalos: [],
        };
    },
    created() {
        const URLAPI = "https://63987b46fe03352a94d2992f.mockapi.io/regalos";
        fetch(URLAPI)
            .then(response => response.json())
            .then(data => {
            console.log(data);
            this.regalos = data;
        });
    },
    components: { CartaRegalo }
};
</script>

<style scoped>

</style>