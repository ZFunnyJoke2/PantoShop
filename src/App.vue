<template>
  <div id="app">
    <TheHeader/>
    <main class="content">
      <FirstPage
          content="Make your interior more
                   minimalistic & modern"
      />
      <FirstPage
          content="Turn your room with panto into a lot more
                   minimalist and modern with ease and speed" />
      <FirstPage
          content=""
          :is-last-page="true"
      />
    </main>
  </div>
</template>

<script>
import FirstPage from './components/FirstPage.vue'
import TheHeader from "@/components/TheHeader.vue";

export default {
  name: 'App',
  components: {
    TheHeader,
    FirstPage
  }
}
</script>

<style>
/* Глобальные стили */
#app {
  font-family: Gilroy-Light, sans-serif;
  text-align: left;
  color: #2c3e50;
  margin: 0;
  background-image: url("assets/img/JOPA.jpg");
}
.content {
  padding: 50px;
}
</style>