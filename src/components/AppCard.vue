<script>
export default {
    name: 'AppCarta',
    props: {
        card: Object,
    }
}
</script>

<template>
    <!-- <div class="col-3 my-3 cards-container'">
        <div class="personal-content">

            <div class="image-card-container">
                <img :src="'http://127.0.0.1:8000/storage/' + card.image" class="card-img-top" :alt="card.title">
            </div>
            <div class="apartment-details">

                <h2 class="card-title">{{ card.description }}</h2>
            </div>

            <div class="card-body">
                <a href="#" class="card-link">Clicca qui per maggiori informazioni</a>
            </div>
        </div>
    </div> -->
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
