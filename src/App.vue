<template>
  <HelloWorld msg="Hello World, here is the news!" />

  <!--Div created to hold all articles.-->
  <div id="articleView">
    <ul>
      <!--
        Unordered list created to hold article components.
        v-for used to render components with JSON file.
      -->
      <li v-for="(article, index) in articles" :key="article._id">     
        
        <!--
          Component gets added with v-if to alternate images.
        -->
        <ArticleComponent v-if="index % 2 === 0"
          :media=article.media
          :title=article.title
          :author=article.author
          :summary=article.summary
          :link=article.link
          :isLeft=true
        />
        <ArticleComponent v-else
          :media=article.media
          :title=article.title
          :author=article.author
          :summary=article.summary
          :link=article.link
          :isLeft=false
        />
      </li>    
    </ul>
  </div>

</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import data from "./assets/data.json";
import ArticleComponent from "./components/ArticleComponent.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    ArticleComponent,
  },
  data() {
    return {
      articles: data,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
