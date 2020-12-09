<template>
  <div id="app">
    <Element color="#e63946" name="first"/>
    <Element color="#457b9d" name="second"/>
    <Element color="#6a994e" name="third"/>
    <Element color="#6930c3" name="fourth"/>
    <Element color="#fca311" name="fifth"/>
    <Element color="#f9c74f" name="sixth"/>
    <Element color="#f15bb5" name="seventh"/>
  </div>
</template>

<script>
import Element from './components/Element.vue'

export default {
  name: 'App',
  components: {
    Element
  }
}
</script>

<style>
#app {
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin-top: 60px;
}
</style>
