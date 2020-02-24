<template>
  <div id="app" ref="app"></div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      greeting: "Hello"
    };
  },
  beforeCreate() {
    console.log("before create", this.$refs.app);
  },
  created() {
    console.log("created", this.$refs.app);
  },
  beforeMount() {
    console.log("before mount", this.$refs.app);
  },
  mounted() {
    console.log("mounted", this.$refs.app);
  },
  watch: {
    greeting: {
      immediate: true,
      handler(to) {
        console.log(to, this.$refs.app);
      }
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
