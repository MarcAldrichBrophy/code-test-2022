<template>
    <div class="article">


    <table>
      <tr>
        
        <!--Image gets added first if isLeft is true.-->
        <td v-if="isLeft">
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
                <p>{{ summary }}</p>
              </td>
            </tr>
            <tr>
              <td>
                <a :href=link>Read More...</a>
              </td>
            </tr>
          </table>
        </td>
        
        <!--Image gets added first if isLeft is false.-->
        <td v-if="!isLeft">
            <img :src=media width="300"/>
        </td>

      </tr>
    </table>
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
    border-radius: 5%;
    
  }

</style>
  