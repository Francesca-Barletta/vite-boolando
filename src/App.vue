<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import FooterApp from './components/FooterApp.vue';

export default {
  components: {
    Header,
    Main,
    FooterApp
  }
}

</script>

<template>
<Header/>
<Main/>
<FooterApp/>
</template>

<style lang="scss">
@use './style/general';

</style>
