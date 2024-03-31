<script>
export default {
    name: 'AppCarta',
    props: {
        // lascia card è già pronto il v-for nella parte main basta solo decomentarlo alla riga 62
        card: Object,
    }
}

</script>


<template lang="">
    <div class="card">
    <img src="" class="card-img-top" alt="">
    <div class="card-body">
        <h5 class="card-title">Nome casa</h5>
    </div>
    <ul class="list-group list-group-flush">
        <li class="list-group-item">Zona casa</li>
    </ul>
    <div class="card-body">
        <a href="#" class="card-link">Clicca qui per maggiori informazioni</a>
    </div>
    </div>
</template>

<style lang="scss"></style>