<template>
    <main class="container">
        <div class="card card-1">
            <h1 class="title text-secondary">ABOUT THE UNIVERSE</h1>
            <p>Bienvenue sur <span class="text-secondary">ABOUT THE UNIVERSE</span> pour découvrir toutes nos découvertes à propos du monde qui nous entoure !</p>
        </div>
        <div class="card card-2">
            <h1 class="title text-secondary">Les chiffres</h1>
            <p>Nous nous efforcons à archiver toutes nos trouvailles pour vous les partager autant que possible !</p>
            <div class="d-grid-2 mt-5 mb-5 w-100">
            <div class="d-grid-2 mt-5 mb-5 w-100">
                <div class="information">
                <span class="fas fa-users fa-3x img text-secondary"></span>
                <div class="ml-3">
                    <div class="bold text-secondary">
                    Nombre d'êtres vivants recensés
                    </div>
                    <div class="info">{{ count }}</div>
                </div>
                </div>
                <div class="information">
                <span class="fas fa-space-shuttle fa-3x img text-secondary"></span>
                <div class="ml-3">
                    <div class="bold text-secondary">
                    Nombre de véhicules recensés
                    </div>
                    <div class="info">3</div>
                </div>
                </div>
            </div>
            <div class="d-grid-2 mt-5 mb-5 w-100">
                <div class="information">
                <span class="fas fa-globe fa-3x img text-secondary mr-3"></span>
                <div>
                    <div class="bold text-secondary">
                    Nombre de planètes recensées
                    </div>
                    <div class="info">3</div>
                </div>
                </div>
                <div class="information">
                <span class="fas fa-clock fa-3x img text-secondary mr-3"></span>
                <div>
                    <div class="bold text-secondary">
                    Prochaine mission
                    </div>
                    <div class="info">10 Juin 2021</div>
                </div>
                </div>
            </div>
            </div>
        </div>
    </main>
</template>

<script>
import axios from 'axios'

export default {
    name: 'HomeView',
    // Les données du composant
    data() {
        return {
            count: 0
        }
    },
    // Les méthodes du composant
    methods: {
        getDataCount() {
            axios.get('https://swapi.dev/api/people')
            .then(response => {
                this.count = response.data.count
            })
        }
    },
    // Méthode qui s'exécute à l'utilisation du composant
    mounted() {
        this.getDataCount();
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
