<template>
  <div class="color">
    <h1>Bonjour je suis dans le app (composant principal)</h1>
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default{
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
.color {
  background-color: aquamarine;
}

.dark {
  background-color: rgb(24, 24, 24);
}
</style>
