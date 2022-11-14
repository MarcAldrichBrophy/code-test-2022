<template>
  <HelloWorld msg="Hello World, here is the news!" />

  <div id="articleView">
    <ul>
      <li v-for="article in articles" :key="article._id">         
        <ArticleComponent
          :media=article.media
          :title=article.title
          :author=article.author
          :summary=article.summary
          :link=article.link
        />
      </li>    
    </ul>
  </div>
  <!--
  <div class="article">
    <table>
      <tr>
        <td>
          <img :src="articles[0].media" width="300" />
        </td>
        <td>
          <table>
            <tr>
              <td>
                <h1>{{ articles[0].title }}</h1>
              </td>
            </tr>
            <tr>
              <td>
                <h3>By {{ articles[0].author }}</h3>
              </td>
            </tr>
            <tr>
              <td>
                <p>By {{ articles[0].summary }}</p>
              </td>
            </tr>
            <tr>
              <td>
                <a :href="articles[0].link">Read More...</a>
              </td>
            </tr>
          </table>
        </td>
      </tr>
    </table>
  </div>
  -->
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
