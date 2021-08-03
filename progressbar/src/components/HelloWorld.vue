<template>
  <v-container class="py-0">
    <v-row align="start" justify="start">
      <v-col
        v-for="i in max"
        :key="i"
        class="pa-0 ma-0 align-start"
        style="padding: 0 !important; margin: 0 !important; flex-grow: 0.04"
      >
        <v-chip :color="colorChip(i)"> </v-chip
      ></v-col>
      <v-col
        style="
          padding-top: 0px;
          padding-bottom: 0px;
          display: flex;
          align-items: center;
        "
      >
        {{ progress }} / {{ max }}
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    max: {
      type: Number,
      default: 10,
    },
    progress: {
      type: Number,
      default: 0,
    },
  },
  methods: {
    colorChip(n) {
      if (n <= this.progress) {
        return "#1867C0";
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
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
