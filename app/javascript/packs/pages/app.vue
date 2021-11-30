<template>
  <div class="md:container md:mx-auto md:content-center">

    <figure class="max-w-5xl md:flex md:justify-between bg-gray-100 rounded-2xl overflow-hidden p-8 md:p-0">
      <img class="w-32 h-32 md:mx-0 md:w-48 md:h-auto md:rounded-none rounded-full mx-auto" src="../../../assets/images/amochi.jpg">
      <div class="pt-6 md:p-8 text-center md:text-left space-y-4 flex flex-col justify-between">
        <blockquote>
          <p class="text-lg font-semibold text-left">
            “{{morning}}” 
            "{{ message }}".
          </p>
        </blockquote>
        <figcaption class="font-medium flex flex-col justify-between">
          <div class="text-cyan-600">
            Amoralchik
          </div>
          <div class="text-gray-500">
            Software Developer, Ukraine
          </div>
        </figcaption>
      </div>
    </figure>
  
  </div>
</template>

<script>

function getMorning() {
  if (new Date().getUTCHours() > 7 && new Date().getUTCHours() < 16) {
    return true
  }
  return false
}

function getMorningMessage(morning) {
    if (morning) return "Have a nice day!"
    return "Time for relax."
}

export default {
  data: function () {
    return {
      message: `Hi, you are in ${new Date().getFullYear()}`,
      morning: getMorningMessage(getMorning())
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
