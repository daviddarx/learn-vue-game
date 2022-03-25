<template>
  <div class="modal">
    <h1 id="header">Finished</h1>
    <h2 v-if="uiState === 'won'">You won!</h2>
    <h2 v-else>You lost!</h2>
    <button @click="restart">Restart</button>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  computed: {
    ...mapState(["uiState"])
  },
  methods: {
    restart() {
      this.$store.commit("restartGame");
    }
  }
};
</script>

<style lang="scss" scoped></style>
