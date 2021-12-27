<template>
  <div id="app">
    <div class="container">
    <Header />

    <main>
      <CharactersList />
    </main>
   

    </div>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue"
import CharactersList from "./components/CharactersList.vue"



export default {
  name: "App",
  components: {
    Header,
    CharactersList,
    
    
  },
};
</script>

<style lang="scss">
@import './style/variables.scss';

@import './style/general.scss';


</style>
