<template>
  <h1>{{ slug }}</h1>
</template>

<script>
export default {
  asyncData ({ params, payload }) {
    const slug = params.slug // When calling /abc the slug will be "abc"
    if (payload) {
      console.log('payload', payload)
    }
    return { slug }
  }
}
</script>
