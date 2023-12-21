<template>
    <div class="card col-2 p-2 m-2">
        <img class='card-img-top' :src="regalo.avatar" alt="avatar">
        <div class="card-body">
            <h4>{{ regalo.destinatario }}</h4>
            <p>{{ regalo.regalo }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CartaRegalo',
    props:{
        regalo:Object,
    },
    data() {
        return {
            
        };
    },

};
</script>

<style scoped>

</style>