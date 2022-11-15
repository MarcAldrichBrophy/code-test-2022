<template>
    <div class="article">

        <div class="articleChild" v-if="isLeft">
          <img style="float: left" :src=media >
        </div>

        <div class="articleChild">
          <h1>{{ title }}</h1>
          <h3>By {{ author }}</h3>
          <p>{{ summary }}</p>
          <a :href=link>Read More...</a>
        </div>
        

        <div class="articleChild" v-if="!isLeft">
          <img style="float: right" :src=media>
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
    width: 300px;
    height: 150px;
    border-radius: 5%;
  }

  .article {
    float: left;
  }

  .articleChild {
    padding: 1rem 1rem;
    text-align: left;
    width: 30%;
    float: left;
    /*height: 1em;*/
  }



</style>
  