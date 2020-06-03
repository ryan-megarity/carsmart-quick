<template>
  <div class="center-block text-center">
    <div v-if="!isMobile()">
      <b-img
      :src="require('../assets/CarsmartLandingPageDesign.jpg')"
      alt="landing page desktop image" fluid-grow>
      </b-img>
    </div>
    <div v-else>
      <b-img
      :src="require('../assets/CarsmartLandingPageDesignMobile2.jpg')"
      alt="landing page mobile image" fluid-grow>
  </b-img>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Home',
  methods: {
    isMobile: () => {
      if (/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        return true;
      }
      return false;
    },
  },
};
</script>
