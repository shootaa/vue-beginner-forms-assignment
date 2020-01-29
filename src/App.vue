<template>
  <div id="app">
    <div class="container">
      <form>
        <!--
          1. Create a product registration form where you have the following fields:
            - Product name (input text)
            - Product's Brand (input text)
            - Price (input text)
            - Colors: Black or White (radio button)

          2. Only display the form if it has not been submitted yet
          3. Make the Data Display below only be visible after the form has been submitted
        -->
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "app"
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
