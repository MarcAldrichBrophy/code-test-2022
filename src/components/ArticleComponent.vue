<template>
    <div class="article">
    <table>
      <tr>
        <td>
          <img :src="articles[0].media" width="300"/>
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
</template>
  
  <script>
  export default {
    name: 'HelloWorld',
    props: {
      msg: String
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
  