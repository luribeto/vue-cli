<template>
  <div>
    <server-status v-for="(server, idx) in 5" v-bind:key="idx"></server-status>
  </div>
</template>

<script>
import ServerStatus from "./ServerStatus.vue";

export default {
  components: {
    "server-status": ServerStatus
  }
};
</script>