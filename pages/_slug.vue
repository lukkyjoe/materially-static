<template>
  <div>
    <h1>{{ slug }}</h1>
    {{ something }}
  </div>
</template>

<script>
export default {
  asyncData ({ params, payload }) {
    const slug = params.slug // When calling /abc the slug will be "abc"
    if (payload) {
      console.log('payload', payload)
    } else {
      console.log('no payload', payload)
    }
    const something = payload ? payload.name : ''
    return { slug, something }
  }
}
</script>
