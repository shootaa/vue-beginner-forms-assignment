<template>
    <div>
        <label for="product-color-black">Black</label>
        <input
          id="product-color-black"
          type="radio"
          value="Black"
          :checked="checked"
          @change="$emit('change',$event.target.value)"
        />
        <label for="product-color-white">White</label>
        <input
          id="product-color-white"
          type="radio"
          value="White"
          :checked="checked"
          @change="$emit('change',$event.target.value)"
         
        />
    </div>
</template>



<script>
export default {
    props:["checked"]
}
</script>