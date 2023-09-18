<template>
  <div class="results">
    <p>Reaction Time :{{ score }}</p>
    <p>{{ rank }}</p>
  </div>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score <= 250) {
      this.rank = "Ninja fingers";
    } else if (this.score <= 400) {
      this.rank = "Rapid reflexes";
    } else {
      this.rank = "slow pace";
    }
  },
};
</script>

<style scoped>
.results {
  align-items: center;
  margin: 1em auto;
  width: 300px;
  border: 1px solid;
  border-radius: 5px;
  background-color: black;
  color: #fff;
}
</style>
