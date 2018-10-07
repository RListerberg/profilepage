<template>
    <v-container fluid>
      <v-img
        class="imgCenter"
        :gradient="gradient"
        src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg">
        <v-layout column align-center >
            <div class="align-content-center">
            <blockquote>
              &#8220;Drink up me hearties, Yoho!!&#8221;
              <footer>
                <small>
                  <em>&mdash;Robin Listerberg</em>
                </small>
              </footer>
            </blockquote>
            </div>
        </v-layout>
      </v-img>
    </v-container>
</template>

<script>
export default {
  name: 'Index',
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
.fluid {
  padding-left: 0;
  padding-right: 0;
}
.imgCenter{
  align-self: center;
}
.v-responsive__content{
  align-self: center
}
</style>
