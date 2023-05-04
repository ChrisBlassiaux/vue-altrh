<template>
  <div class="color-2">
    <h2>Bonjour {{ name }}, vous avez {{ age }} ans. </h2>
    <p>Vous êtes majeur : {{ isMajor }} </p>
    <p>Vous êtes passionné.e de {{ hobbies.art }}</p>
    <button @click="mode($event)">Mode dark / light</button>
    <input type="text" :value="description">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {},
  data() {
    return {
      name: 'Marina',
      age: 24,
      isMajor: true,
      hobbies: {
        art: 'Peinture'
      },
      description: 'Bonjour, je m\'appelle...'
    }
  },
  methods: {
    mode(event) {
      console.log(event);
      document.body.classList.toggle('dark');
    }
  },
  mounted() {
    console.log('Salut!');
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.color-2 {
  background-color: blueviolet;
}

</style>
