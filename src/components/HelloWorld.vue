<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <Accordion
      :openedTitle="'Hide Code'"
      :closedTitle="'Show Code'">
      <div slot="content">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tenetur, architecto, explicabo perferendis nostrum, maxime impedit atque odit sunt pariatur illo obcaecati soluta molestias iure facere dolorum adipisci eum? Saepe, itaque.
      </div>
    </Accordion>

    <Button
      :variation="'default'">
      Default
    </Button>
  </div>
</template>

<script>
import { Accordion, Button } from "streamlabs-beaker";

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    Accordion,
    Button,
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
