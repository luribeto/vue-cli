<template>
  <div>
    <p>
      Server Status:
      <span v-bind:class="classObject">{{ status }}</span>
    </p>
    <button @click="changeStatus">Change Status</button>
    <hr />
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      status: "Normal"
    };
  },
  methods: {
    changeStatus() {
      const currentStatus = this.status;
      this.status = currentStatus === "Normal" ? "Critical" : "Normal";
    }
  },
  computed: {
    classObject: function() {
      return {
        danger: this.status === "Critical",
        normal: this.status !== "Critical"
      };
    }
  }
};
</script>