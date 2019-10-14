<template>
  <div class="container">{{ films }}</div>
</template>

<script>
import films from "@/data/films.json";

export default {
  data() {
    return {
      films
    };
  }
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
