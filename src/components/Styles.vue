<template>
  <div class="hello">
    <input class="padding-top" type="number" v-model="paddingTop" />
    <input class="padding-right" type="number" v-model="paddingRight" />
    <input class="padding-bottom" type="number" v-model="paddingBottom" />
    <input class="padding-left" type="number" v-model="paddingLeft" />

    <div
      class="preview"
      :style="{
        'border-top-width': paddingTop + 'px',
        'border-right-width': paddingRight + 'px',
        'border-bottom-width': paddingBottom + 'px',
        'border-left-width': paddingLeft + 'px'
      }"
    ></div>
  </div>
</template>

<script>
export default {
  name: "Styles",
  data() {
    return {
      paddingTop: 1,
      paddingRight: 1,
      paddingBottom: 1,
      paddingLeft: 1
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.preview {
  border: 1px solid blue;
  width: 200px;
  height: 200px;
  margin: 20px auto;
}
</style>
