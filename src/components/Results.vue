<template>
  <P>Your Reaction Time is {{ score }} ms</P>
  <p class="rank">{{ rank }}</p>
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
    if (this.score < 250) {
      this.rank = " Your A Ninja";
    } else if (this.score < 400) {
      this.rank = "Not bad for an olden!!!";
    } else {
      this.rank = "Man you are slow!!!";
    }
  },
};
</script>

<style>
.rank {
  font-size: 2rem;
  color: #0faf87;
  font-weight: bold;
}
</style>
