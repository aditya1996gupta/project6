<template>
  <!-- myResolvedValue be "No fanciness" until it resolves. -->
  <h2>Asynchronous Property default value {{myResolvedValue}}</h2>
</template>

<script>
export default {
  asyncComputed: {
    myResolvedValue: {
      get () {
        return new Promise((resolve, reject) => {
          setTimeout(() => resolve('*Fancy* Resolved Value!'), 4000)
        })
      },
      default: 'No fanciness'
    }
  }
}
</script>
