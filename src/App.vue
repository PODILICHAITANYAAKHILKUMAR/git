<template>
  <div class="modal">
    <!-- Modal content -->
    <multiselect
      v-model="selectedOptions"
      :options="options"
      label="name"
      track-by="id"
      :multiple="false"
    ></multiselect>
  </div>
</template>

<script>
import Multiselect from "vue-multiselect";

export default {
  components: {
    Multiselect,
  },
  data() {
    return {
      selectedOptions: [],
      options: [
        // Your options here
        "1",
        "2",
        "3",
      ],
    };
  },
  // Other modal logic
};
</script>

<style scoped>
/* Modal styles */
.modal {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: white;
  padding: 20px;
  z-index: 1000;
}

/* Override vue-multiselect styles */
.multiselect {
  position: fixed; /* Position dropdown outside modal */
  top: 0;
  left: 0;
  z-index: 2000; /* Ensure it's above the modal */
}
</style>
