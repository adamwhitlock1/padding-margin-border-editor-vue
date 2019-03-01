<template>
  <div class="hello">
    <p>Margin</p>
    <input class="margin-top" type="number" v-model="marginTop" />
    <input class="margin-right" type="number" v-model="marginRight" />
    <input class="margin-bottom" type="number" v-model="marginBottom" />
    <input class="margin-left" type="number" v-model="marginLeft" />

    <p>Padding</p>
    <input class="padding-top" type="number" v-model="paddingTop" />
    <input class="padding-right" type="number" v-model="paddingRight" />
    <input class="padding-bottom" type="number" v-model="paddingBottom" />
    <input class="padding-left" type="number" v-model="paddingLeft" />

    <button @click="paddingChangeLink">{{ linkPadding }}</button>

    <div class="container">
      <div
        class="marginPreview"
        :style="{
          'border-top-width': marginTop + 'px',
          'border-right-width': marginRight + 'px',
          'border-bottom-width': marginBottom + 'px',
          'border-left-width': marginLeft + 'px'
        }"
      >
        <div
          class="paddingPreview"
          :style="{
            'border-top-width': paddingTop + 'px',
            'border-right-width': paddingRight + 'px',
            'border-bottom-width': paddingBottom + 'px',
            'border-left-width': paddingLeft + 'px'
          }"
        ></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Styles",
  data() {
    return {
      marginTop: 1,
      marginRight: 1,
      marginBottom: 1,
      marginLeft: 1,

      paddingTop: 1,
      paddingRight: 1,
      paddingBottom: 1,
      paddingLeft: 1,

      linkPadding: "Click to link"
    };
  },
  methods: {
    paddingChangeLink() {
      console.log(this.linkPadding);
      if (this.linkPadding === "Click to link") {
        this.linkPadding = "Click to unlink";
      } else {
        this.linkPadding = "Click to link";
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  margin: 0 15%;
}
.paddingPreview {
  border: 1px solid blue;
  margin: 20px;
  padding: 30px;
}

.borderPreview {
  border: 1px solid blue;
  margin: 20px;
}

.marginPreview {
  border: 1px solid orange;
  margin: 20px;
  padding: 10px;
}
</style>
