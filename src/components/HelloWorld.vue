<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <Accordion :opened-title="'Close Accordion'" :closed-title="'Open Accordion'">
      <div slot="content">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>
    </Accordion>
    <button-input :variation="'default'" :title="'Button'"></button-input>

    <ProgressBar :progressComplete="progress"></ProgressBar>

    <VirtualItem
      v-for="(mask, id) in masks"
      :key="id"
      :preview="mask.preview"
      :rarity="mask.rarity"
      :name="mask.name"
      :selectionCount="mask.selectionCount"
      :selected="mask.selected"
      @click="clickEvent(mask)"
    ></VirtualItem>
    <NewFeatureOverlay
      :label="'Introducing Cloudbot'"
      :title="'Your Favorite Bot is Now Available in the Cloud'"
      :media="'https://www.youtube.com/embed/dWZNtpNRpG8'"
    >
      <slot>We’ve worked with some of the best developers in the industry to bring you the tools to take your stream to the next level.
        <br>
        <br>We’ve automatically credited $15.00 to your account so you can start trying them out today. We’ve automatically credited $15.00 to your account so you can start trying them out today.
      </slot>
    </NewFeatureOverlay>

    <Button
      :variation="'default'"
      :title="'New Feature Overlay'"
      @click="$modal.show('new-feature')"
    ></Button>
  </div>
</template>

<script>
import {
  Accordion,
  Button,
  ProgressBar,
  ItemGrid,
  VirtualItem,
  NewFeatureOverlay
} from "streamlabs-beaker";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  components: {
    Accordion,
    "button-input": Button,
    ProgressBar,
    VirtualItem,
    ItemGrid,
    NewFeatureOverlay
  },

  data() {
    return {
      progress: 23,
      masks: [
        {
          preview: "https://streamlabs.com/imgs/facemasks/robot-mask.png",
          name: "Robot",
          rarity: "Common",
          selectionCount: "1",
          selected: true
        },
        {
          preview: "https://streamlabs.com/imgs/facemasks/robot-mask.png",
          name: "Robot",
          rarity: "Common",
          selectionCount: "2",
          selected: true
        },
        {
          preview: "https://streamlabs.com/imgs/facemasks/robot-mask.png",
          name: "Robot",
          rarity: "Common",
          selectionCount: "3",
          selected: true
        },
        {
          preview: "https://streamlabs.com/imgs/facemasks/robot-mask.png",
          name: "Robot",
          rarity: "Common"
        },
        {
          preview: "https://streamlabs.com/imgs/facemasks/robot-mask.png",
          name: "Robot",
          rarity: "Common"
        },
        {
          preview: "https://streamlabs.com/imgs/facemasks/robot-mask.png",
          name: "Robot",
          rarity: "Common"
        },
        {
          preview: "https://streamlabs.com/imgs/facemasks/robot-mask.png",
          name: "Robot",
          rarity: "Common"
        },
        {
          preview: "https://streamlabs.com/imgs/facemasks/robot-mask.png",
          name: "Robot",
          rarity: "Common"
        }
      ]
    };
  },

  methods: {
    clickEvent(mask) {
      mask.key = 4;
    }
  }
};
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
