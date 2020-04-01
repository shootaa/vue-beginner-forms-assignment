<template>
  <div>
    <label for="product-brand">Product Name</label>
    <input
      id="product-brand"
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
