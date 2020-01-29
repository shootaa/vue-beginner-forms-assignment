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
             and make it display all the submitted data
        -->
      </form>

      <div class="data-display">
        <div class="data-container">
          <h2 class="title">Submitted Data</h2>

          <div class="data-content">
            <p>
              <span>Product Name:</span>
              <!-- Display the product Nname here -->
            </p>

            <p>
              <span>Product Brand:</span>
              <!-- Display the product brand here -->
            </p>

            <p>
              <span>Product Price:</span>
              <!-- Display the product price here -->
            </p>

            <p>
              <span>Product Color:</span>
              <!-- Display the Product color here-->
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app"
};
</script>

<style lang="scss">
$border: #dcdcdc;

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
  display: flex;
  justify-content: center;

  form,
  .data-display {
    border: 1px solid $border;
    width: 370px;
    margin: 0 15px;
    border-radius: 5px;
    padding: 15px 30px;
  }

  .data-display {
    max-height: 225px;

    .data-container {
      .title {
        text-align: center;
      }

      p {
        & > span {
          font-weight: bold;
        }
      }
    }
  }
}
</style>
