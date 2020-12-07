<template>

    <div class="card">
        <!-- <div>{{member}}</div> -->
        <img src= "" class="card-img-top" alt="foto">
        <div class="card-body">
            <h5 class="card-title">Codigo: {{member.codigo}}</h5>
            <h5 class="card-title"> {{member.nombre}} </h5>
            <h6 class="card-title"> {{member.rol}} </h6>
            <p class="card-text">{{member.descripcion}}</p>
        </div>
    </div>
    
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

</style>
