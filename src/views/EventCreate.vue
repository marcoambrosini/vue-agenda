<template>
  <div>
    <h1>Create Event {{user.namne}}</h1>
    <p>This event was created by {{user.id}}</p>
    <p>There are {{catLength}} categories</p>
  </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
  computed: {
    catLength() {
      return this.$store.getters.catLength;
    },
    ...mapState(['user', 'categories'])
  }
};
</script>

<style lang="scss" scoped>
</style>
