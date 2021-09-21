<template>
  <div class="hello">
    <h1>AR Preview</h1>
    <div>
      <input v-model="message" placeholder="http://demo.example/...">
      <a :href="message" rel="ar">Click to view AR.</a>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data: () => ({
    message: "",
  }),
  methods: {
    selectFile() {
      let fileInputElement = this.$refs.file as any;
      fileInputElement.click();

      // Do something with chosen file
      console.log(fileInputElement.files);
    },
  },
});
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
