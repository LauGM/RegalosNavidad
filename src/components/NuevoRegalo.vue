<template>
    <div>
        <form @submit.prevent="postear">
            <h2>Nuevo Regalo</h2>
            <label for="nombre">
                Para quien es el regalo:
                <input class="form-control" v-model="nombre" name='nombre' type="text" placeholder="Juan">
            </label>
            <label for="regalo">
                Que le quiero regalar:
                <input class="form-control" v-model='regalo' type="text" name="regalo" placeholder="Mochila">
            </label>
            <input class="btn btn-warning" type="submit" value="CARGAR">
        </form>
    </div>
</template>

<script>
export default {
    name: 'NuevoRegalo',

    data() {
        return {
            nombre:'',
            regalo:'',
        };
    },
    methods:{
        async postear(){
            const nuevoRegalo={
                destinatario:this.nombre,
                regalo:this.regalo
            }
            console.log(nuevoRegalo);
            const response=await fetch('https://63987b46fe03352a94d2992f.mockapi.io/regalos',{
                method:'POST',
                body:JSON.stringify(nuevoRegalo),
                headers: {"Content-type": "application/json; charset=UTF-8"}
            });
            const data=await response.json();
            console.log(data);
            alert('Nuevo regalo enviado a la API');
            location.reload();
        }
    }
};
</script>

<style scoped>

</style>