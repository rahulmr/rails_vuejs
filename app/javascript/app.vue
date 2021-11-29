<template>
  <div id="app">
    <div class="container">
      <h1>{{ message }}</h1>
    </div>
    <div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium odio quae maxime ad perspiciatis, sed tempore in iure, libero veritatis natus dolores quasi pariatur perferendis quis repellat aut quod error.</p>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Blanditiis eaque veritatis ducimus? Quae nemo ullam, illum voluptas odit ex, voluptatum recusandae delectus ea, impedit dolorem voluptatem at possimus. Non, quaerat.</p>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      message: `Hi, you are in ${new Date().getFullYear()}`
    }
  }
}
</script>

<style scoped>
p {
  font-size: 2em;
  text-align: center;
}
</style>
