<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <Accordion>
      <div slot="toggle">
        Accordion Title
      </div>
      <div slot="content">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tenetur, architecto, explicabo perferendis nostrum, maxime impedit atque odit sunt pariatur illo obcaecati soluta molestias iure facere dolorum adipisci eum? Saepe, itaque.
      </div>
    </Accordion>
  </div>
</template>

<script>
import Vue from "vue";
import { Accordion } from "streamlabs-beaker";
Vue.use(Accordion);

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },

  mounted() {
    console.log(Accordion)
  },
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
