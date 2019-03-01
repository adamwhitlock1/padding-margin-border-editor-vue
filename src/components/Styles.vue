<template>
  <div class="hello">
    <input class="padding-top" type="text">
    <input class="padding-right" type="text">
    <input class="padding-bottom" type="text">
    <input class="padding-left" type="text">

    <div class="preview" :style={border-size-top: "padding-top"} >
    </div>


  </div>
</template>

<script>
export default {
  name: "Styles",
  props: {
    msg: String
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
