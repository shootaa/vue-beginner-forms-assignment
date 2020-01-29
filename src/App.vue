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
        <label for="product-name">
          Product Name
        </label>

        <label for="product-brand">
          Product Brand
        </label>

        <label for="product-color-black">
          Black
        </label>

        <label for="product-color-white">
          White
        </label>

        <button @click.prevent="submitForm">Submit</button>
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
  name: "app",
  methods: {
    submitForm() {}
  }
};
</script>

<style lang="scss">
$border: #dcdcdc;

body {
  * {
    box-sizing: border-box;
  }
}

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

  form {
    input[type="text"] {
      width: 100%;
      max-width: 100%;
      height: 30px;
      border-radius: 5px;
      border: 1px solid $border;
      padding: 5px 15px;
      margin: 5px 0 15px;

      label {
        font-size: 14px;
        font-weight: 500;
      }
    }

    input {
      transition: 0.3s ease;

      &:hover {
        border-color: #000000;
      }
    }

    button {
      width: 100%;
      height: 30px;
      border: 1px solid $border;
      margin: 30px 0 5px;
      transition: 0.3s ease;

      &:hover {
        border-color: #000000;
      }
    }
  }

  .data-display {
    max-height: 300px;

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
