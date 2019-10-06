<template>
  <div class="spotify-item">

  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.spotify-item {
  display: flex;
  flex-direction: column;
  .cover {
    width: 100%;
  }
  .title {
    color: white;
  }
  .details {
    color: rgb(155, 155, 155);
    .caption {
      line-clamp: 3;
      display: -webkit-box;
      text-align: justify;
      -webkit-line-clamp: 3;
      -webkit-box-orient: vertical;
    }
    .followers {
      text-transform: uppercase;
      letter-spacing: 2em;
    }
  }
}
</style>
