<template>
  <div>
    <label for="product-name">Product Name</label>
    <input
      id="product-name"
      type="text"
      :value="value"
      @input="$emit('input',$event.target.value)"
    />
  </div>
</template>

<script>
export default {
    props:["value"]
};
</script>
