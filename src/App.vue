<template>
  <div id="app">
    <div class="container">
      <form v-if="!isSubmitted">
        <label for="product-name">
          Product Name
          <input
            id="product-name"
            name="product-name"
            type="text"
            placeholder="Product name"
            v-model="product.name"
          />
        </label>

        <label for="product-brand">
          Product Brand
          <input
            id="product-brand"
            name="product-brand"
            type="text"
            placeholder="Product brand"
            v-model="product.brand"
          />
        </label>

        <label for="product-price">
          Product Price
          <input
            id="product-price"
            name="product-price"
            type="text"
            placeholder="Product price"
            v-model="product.price"
          />
        </label>

        <label for="product-color-black">
          Black
          <input
            id="product-color-black"
            name="product-color-black"
            type="radio"
            value="Black"
            v-model="product.color"
          />
        </label>

        <label for="product-color-white">
          White
          <input
            id="product-color-white"
            name="product-color-white"
            type="radio"
            value="White"
            v-model="product.color"
          />
        </label>

        <button @click.prevent="submitForm">Submit</button>
      </form>

      <div class="data-display" v-if="isSubmitted">
        <div class="data-container">
          <h2 class="title">Submitted Data</h2>

          <div class="data-content">
            <p>
              <span>Product Name:</span>
              {{ product.name }}
            </p>

            <p>
              <span>Product Brand:</span>
              {{ product.brand }}
            </p>

            <p>
              <span>Product Price:</span>
              {{ product.price }}
            </p>

            <p>
              <span>Product Color:</span>
              {{ product.color }}
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
  data() {
    return {
      isSubmitted: false,
      product: {
        name: "",
        brand: "",
        price: "",
        color: ""
      }
    };
  },
  methods: {
    submitForm() {
      this.isSubmitted = true;
    }
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
    max-height: 250px;

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
