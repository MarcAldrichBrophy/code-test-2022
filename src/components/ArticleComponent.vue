<template>
    <div class="article">
    <table>
      <tr>
        <td>
          <img :src=media width="300"/>
        </td>
        <td>
          <table>
            <tr>
              <td>
                <h1>{{ title }}</h1>
              </td>
            </tr>
            <tr>
              <td>
                <h3>By {{ author }}</h3>
              </td>
            </tr>
            <tr>
              <td>
                <p>By {{ summary }}</p>
              </td>
            </tr>
            <tr>
              <td>
                <a :href=link>Read More...</a>
              </td>
            </tr>
          </table>
        </td>
      </tr>
    </table>
  </div>
</template>
  
  <script>
  export default {
    name: 'ArticleComponent',
    props: {
      media: String,
      title: String,
      author: String,
      summary: String,
      link: String
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
  </style>
  