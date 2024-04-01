<script>
export default {
    name: 'AppCarta',
    props: {
        card: Object,
    }
}
</script>

<template>

    <div class="col-sm-12 col-md-6 col-lg-3 col-xl-3 my-3">
    <div class="card">
        <!-- Usa :src per il binding dinamico dell'attributo src e :alt per l'alt -->
        <!-- Nota l'uso della notazione punto per accedere alle proprietà dell'oggetto card -->
        <img :src="'http://127.0.0.1:8000/storage/' + card.image"  class="card-img-top" :alt="card.title">
        <div class="card-body">
            <!-- Qui l'interpolazione con {{ }} è corretta perché è nel contenuto di un elemento -->
            <h5 class="card-title">{{ card.description }}</h5>

        </div>
    </div> 
    <div class="col-sm-12 col-md-6 col-lg-3 col-xl-3 my-3">
        <div class="card">
            <img :src="'http://127.0.0.1:8000/storage/' + card.image" class="card-img-top" :alt="card.title">
            <div class="card-body">
                <h5 class="card-title">{{ card.location }}</h5>
                <p class="card-text">{{card.description}}</p>
                <a href="#" class="btn btn-primary">Maggiori informazioni</a>
            </div>
        </div>
    </div>

</template>

<style lang="scss">
/* Qui puoi aggiungere lo stile specifico per il tuo componente */
</style>
