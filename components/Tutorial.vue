<!-- Please remove this file from your project -->
<template>
  <div
    class="
      relative
      flex
      items-top
      justify-center
      min-h-screen
      bg-gray-100
      sm:items-center sm:pt-0
    "
  >
    <Editor :value="value" :plugins="plugins" @change="handleChange" />
  </div>
</template>

<script>
import "bytemd/dist/index.css";
import { Editor, Viewer } from "@bytemd/vue";
import mermaid from "@bytemd/plugin-mermaid";
const plugins = [
  mermaid(),
  // Add more plugins here
];

export default {
  components: { Editor },
  name: "NuxtTutorial",
  data() {
    return { value: "", plugins };
  },
  methods: {
    handleChange(v) {
      this.value = v;
    },
  },
};
</script>
