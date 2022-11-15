<template>
    <div class="article">

        <div class="imageChild" v-if="!isLeft">
          <img style="float: right" :src=media>
        </div>

        <div class="articleChild">
          <h1>{{ title }}</h1>
          <h3>By {{ author }}</h3>
          <p>{{ summary }}</p>
          <a :href=link>Read More...</a>
        </div>
        

        <div class="imageChild" v-if="isLeft">
          <img style="float: left" :src=media>
        </div>

    </div>
  
</template>
  
<script>
    // Props added to render component with JSON file.
  export default {
    name: 'ArticleComponent',
    props: {
      media: String,
      title: String,
      author: String,
      summary: String,
      link: String,
      isLeft: Boolean
    }
  }
</script>
  
<style scoped>
  h1 {
    background-color: yellow;
  }
  p {
    font-style: italic;
  }
  img {
    width: 400px;
    height: 200px;
    border-radius: 5%;
    margin-top: 15%;
  }

  .article {
    float: left;
    display: flex;
    justify-content: center;
  }

  .articleChild {
    padding: 1rem 1rem;
    text-align: left;
    width: 35%;
    height: 5%;
    float: left;
  }
  .imageChild {
    padding: 1rem 1rem;
    text-align: left;
    width: 35%;
    float: left;
    display: flex;
    justify-content: center;
  }


</style>
  