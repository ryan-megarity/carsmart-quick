<template>
  <div>
    <nav class="navbar navbar-light bg-light fixed-top">
      <div class="navbar-brand">
        <a class="navbar-brand" href="/">
          <img src="../assets/carsmart logo_Sml_crop.png" width="125px" alt="carsmart logo">
        </a>
      </div>
      <div class="navbar-brand">
      <a @click="showContact=true" class="nav-link">
        <b-button type="button" id="show-btn"
        @click="showModal"
        class="btn btn-outline-primary btn-xs"
        style="font-weight:bold" >Contact</b-button>
      </a>
      <b-modal ref="my-modal" hide-footer title="Contact">
        <div class="d-block text-center">
          <contact/>
        </div>
        <b-button class="mt-3" variant="outline-info" block @click="hideModal">Close Me</b-button>
      </b-modal>
      </div>
    </nav>
    <br><br><br>
  </div>
</template>

<script>
import contact from '@/components/Contact.vue';

export default {
  name: 'topNav',
  components: {
    contact,
  },
  data: () => ({
    showContact: false,
  }),
  methods: {
    showModal() {
      this.$refs['my-modal'].show();
    },
    hideModal() {
      this.$refs['my-modal'].hide();
    },
    toggleModal() {
      // We pass the ID of the button that we want to return focus to
      // when the modal has hidden
      this.$refs['my-modal'].toggle('#toggle-btn');
    },
  },
};
</script>
