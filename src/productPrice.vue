<template>
  <div>
    <label for="product-price">Product Price</label>
    <input id="product-price" type="text" :value="value"
    @input="$emit('input',$event.target.value)"/>
  </div>
</template>

<script>
export default {
  props: ["value"]
};
</script>
