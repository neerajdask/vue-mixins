<template>
  <user-alert v-if="alertIsVisible" :title="alertTitle" @close="hideAlert">
    <p>Do you want to continue with deleting a user?</p>
  </user-alert>
  <section>
    <h2>Delete a User</h2>
    <button @click="showAlert">Delete User</button>
  </section>
</template>

<script>
import AlertMixin from '../mixins/alert';
import UserAlert from './UserAlert.vue';
export default {
  components: { UserAlert },
  data() {
    return {
      alertTitle: 'Delete User!',
    };
  },
  mixins: [AlertMixin],
};
</script>