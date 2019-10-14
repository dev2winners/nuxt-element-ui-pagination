<template>
  <div class="container">
    <div v-for="film in films" :key="film.id" class="films">
      <el-card :body-style="{ padding: '0px' }">
        <img
          src="https://www.downloadwallpapers.info/preview/2015/11/10/810396_overallsite-ps3_1920x1080_h.jpg"
          class="image"
        />
        <div style="padding: 14px;">
          <span class="name">{{ film.name }}</span>
          <span class="actors">{{ film.actors }}</span>
          <span class="genres">{{ film.genres }}</span>
          <span class="description">{{ film.description }}</span>
        </div>
      </el-card>
    </div>
  </div>
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

<style lang="scss">
.container {
  font-family: "Montserrat", "Verdana", "Arial";
  margin: 0 auto;
  min-height: 100vh;
  // display: flex;
  justify-content: center;
  align-items: center;
  text-align: left;
  .films {
    max-width: 400px;
    margin-bottom: 20px;
  }
  span {
    display: block;
  }
  .name {
    font-size: 1.3em;
    font-weight: 500;
    color: #777;
    padding-bottom: 5px;
  }
  .actors {
    font-size: 0.9em;
    font-weight: 400;
    color: #444;
    padding-bottom: 5px;
  }
  .genres {
    font-size: 0.7em;
    font-weight: 600;
    color: #444;
    padding-bottom: 5px;
  }
  .description {
    font-size: 0.9em;
    font-weight: 400;
    color: #444;
    line-height: 1.63;
  }
  .image {
    width: 100%;
  }
}
</style>
