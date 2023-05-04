<template>
  <div class="color-2">
    <h2>Bonjour {{ name }}, vous avez {{ age }} ans. </h2>
    <p>Vous êtes majeur : {{ isMajor }} </p>
    <p>Vous êtes passionné.e de {{ hobbies.art }}</p>
    <button @click="mode($event)">Mode dark / light</button>
    <input type="text" :value="description">

    <!-- Exercice 1 -->
    <h3>Exo1</h3>
    <input type="text" @input="changeColor($event)">
    <div class="square" :style="{ backgroundColor: squareColor }"></div>
    
    <!-- Exercice 2 -->
    <h3>Exo2</h3>
    <button @click="showHello = !showHello">Apparition/disparition du Hello!</button>
    <div class="hello" v-if="showHello">Hello !</div>

    <!-- Exercice 3 -->
    <ul>
      <li v-for="user in users" :key="user">{{ user.firstName }} {{ user.lastName }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {},
  // Les données du composant
  data() {
    return {
      name: 'Marina',
      age: 24,
      isMajor: true,
      hobbies: {
        art: 'Peinture'
      },
      description: 'Bonjour, je m\'appelle...',
      // Exercice 1 
      squareColor: 'grey',
      // Exercice 2 
      showHello: true,
      // Exercice 3
      users: [
        {
          firstName: 'chris',
          lastName: 'b'
        },
        {
          firstName: 'chris',
          lastName: 'b'
        },
        {
          firstName: 'chris',
          lastName: 'b'
        }
      ]
    }
  },
  // Les méthodes du composant
  methods: {
    mode(event) {
      console.log(event);
      document.body.classList.toggle('dark');
    },
    // Exercice 1
    changeColor(event) {
      this.squareColor = event.target.value;
    }
  },
  // Méthode qui s'exécute à l'utilisation du composant
  mounted() {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.color-2 {
  background-color: blueviolet;
}
.square {
  height: 200px;
  width: 200px;
}

.hello {
  background-color: red;
}
</style>
