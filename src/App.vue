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
          content="Let's search furniture!"
          :is-last-page="true"
      />
      <HorizontalBlocks :blocks="horizontalBlocks" />
      <CheckBoxUsage/>
    </main>
  </div>
</template>

<script>
import FirstPage from './components/FirstPage.vue';
import TheHeader from "@/components/TheHeader.vue";
import HorizontalBlocks from './components/HorizontalBlocks.vue';
import CheckBoxUsage from "@/components/CheckBoxUsage.vue";


export default {
  name: 'App',
  components: {
    TheHeader,
    FirstPage,
    HorizontalBlocks,
    CheckBoxUsage
  },
  data() {
    return {
      horizontalBlocks: [
        { title: 'Why', content: 'Choosing us' },
        { title: 'Luxury facilities', content: 'The advantage of hiring a workspace with us is that givees you comfortable service and all-around facilities.' },
        { title: 'Affordable Price', content: 'You can get a workspace of the highst quality at an affordable price and still enjoy the facilities that are oly here.' },
        { title: 'Many Choices', content: 'We provide many unique work space choices so that you can choose the workspace to your liking.' }
      ]
    };
  }
};
</script>

<style>
#app {
  font-family: Gilroy-Light, sans-serif;
  text-align: left;
  color: #2c3e50;
  margin: -10px 0 0 -10px;
  background-image: url("assets/img/JOPA.jpg");
  background-repeat: no-repeat;
}
.content {
  padding: 50px;
}
</style>