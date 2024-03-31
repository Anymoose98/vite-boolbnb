<script>
export default {
    name: 'AppCarta',
    props: {
        card: Object,
    }
}
</script>

<template>
    <div class="card">
        <!-- Usa :src per il binding dinamico dell'attributo src e :alt per l'alt -->
        <!-- Nota l'uso della notazione punto per accedere alle proprietà dell'oggetto card -->
        <img :src="card.image" class="card-img-top" :alt="card.title">
        <div class="card-body">
            <!-- Qui l'interpolazione con {{ }} è corretta perché è nel contenuto di un elemento -->
            <h5 class="card-title">{{ card.description }}</h5>
        </div>
        <ul class="list-group list-group-flush">
            <li class="list-group-item">Zona casa</li>
        </ul>
        <div class="card-body">
            <a href="#" class="card-link">Clicca qui per maggiori informazioni</a>
        </div>
    </div>
</template>

<style lang="scss">
/* Qui puoi aggiungere lo stile specifico per il tuo componente */
</style>
