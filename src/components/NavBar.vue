<template>
    <div class="navbar-height"></div>
    <div class="navbar">
        <div class="contain-burger">
            <div class="burger"></div>
        </div>
        <nav class="nav">
            <img src="../assets/logo.png" alt="Logotype" />
            <router-link to="/" class="navbar-link active">Accueil</router-link>
        </nav>
        </div>
        <nav class="vertical-navbar">
        <router-link to="/planets" class="nav-vertical-link">
            <span class="fas fa-globe fa-3x"></span>
            <p>Planètes</p>
        </router-link>
        <a href="#" class="nav-vertical-link">
            <span class="fas fa-rocket fa-3x"></span>
            <p>Véhicules</p>
        </a>
        <a href="#" class="nav-vertical-link">
            <span class="fab fa-reddit-alien fa-3x"></span>
            <p>Personnes</p>
        </a>
    </nav>
</template>

<script>
export default {
    name: 'NavBar',
    props: {},
    // Les données du composant
    data() {
        return {
            
        }
    },
    // Les méthodes du composant
    methods: {

    },
    // Méthode qui s'exécute à l'utilisation du composant
    mounted() {
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
