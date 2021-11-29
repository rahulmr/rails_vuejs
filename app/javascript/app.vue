<template>
  <div>

    <div class="m-5 mt-10 p-2 grid border-4 border-black rounded-xl bg-blue-500 text-white" id="app">
      <div class='mb-5'>
        <h1 class="text-center text-4xl">vue testing polygon</h1>
      </div>
      <div>
        <p> {{morning}} </p>
      </div>
    </div>

    <div class="m-5 p-2 grid border-4 border-black rounded-xl bg-pink-700 text-white" id="app">
      <div class='mb-5'>
        <h1 class="text-center text-4xl">{{ message }}</h1>
      </div>
      <div>
        <p class='mb-5'>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium odio quae maxime ad perspiciatis, sed tempore in iure, libero veritatis natus dolores quasi pariatur perferendis quis repellat aut quod error.</p>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Blanditiis eaque veritatis ducimus? Quae nemo ullam, illum voluptas odit ex, voluptatum recusandae delectus ea, impedit dolorem voluptatem at possimus. Non, quaerat.</p>
      </div>
    </div>
  
  </div>
</template>

<script>

function getMorning() {
  console.log(new Date().getUTCHours());
  if (new Date().getUTCHours() > 7 && new Date().getUTCHours() < 16) {
    return true
  }
  return false
}

export default {
  data: function () {
    return {
      message: `Hi, you are in ${new Date().getFullYear()}`,
      morning: getMorning()
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
