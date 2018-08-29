<template>
    <v-container fluid>
      <v-responsive>
        <v-layout column align-center>
            <blockquote>
              &#8220;First, solve the problem. Then, write the code.&#8221;
              <footer>
                <small>
                  <em>&mdash;Robin Listerberg</em>
                </small>
              </footer>
            </blockquote>
        </v-layout>
      </v-responsive>  
    </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: () => ({
    gradient: 'to top right, rgba(63,81,181, .7), rgba(25,32,72, .7)'
  }),
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
