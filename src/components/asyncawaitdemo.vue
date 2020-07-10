<template>
  <!-- myResolvedValue will become "*Fancy* Resolved Value!" after one second. -->
  <h2>Asynchronous Property using async/await {{myResolvedValue}}</h2>
</template>

<script>
function fancinessComesLater () {
  return new Promise((resolve, reject) => {
    setTimeout(() => resolve('*Fancy* Resolved Value!'), 2000)
  })
}

export default {
  asyncComputed: {
    async myResolvedValue () {
      return await fancinessComesLater()
    }
  }
}
</script>
