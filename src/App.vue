<template>
  <div id="app" class="justify-content-center background">
    <topNav/>
    <Home/>
  </div>
</template>

<script>
// @ is an alias to /src
import Home from '@/views/Home.vue';
import topNav from '@/components/topNav.vue';

export default {
  name: 'App',
  components: {
    Home,
    topNav,
  },
};
</script>
