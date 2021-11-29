<template>
  <div class="p-24">

    <figure class="md:flex bg-gray-100 rounded-2xl p-8 md:p-0">
      <img class="w-32 h-32 md:w-48 md:h-auto md:rounded-none rounded-full mx-auto" src="../assets/images/amochi.jpg" alt="" width="384" height="512">
      <div class="pt-6 md:p-8 text-center md:text-left space-y-4">
        <blockquote>
          <p class="text-lg font-semibold text-left">
            “Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Quasi, quos nulla dolore repudiandae voluptates voluptatum?
            Porro sunt, unde recusandae beatae odio repellendus qui atque doloremque laborum.
            Voluptates culpa voluptatibus enim.”
          </p>
        </blockquote>
        <figcaption class="font-medium">
          <div class="text-cyan-600">
            Amoralchik
          </div>
          <div class="text-gray-500">
            Software Developer, Ukraine
          </div>
        </figcaption>
      </div>
    </figure>

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
