<template>
  <div>
    <h1>ID is: {{ id }}</h1>
  </div>
</template>

<script>
export default {
  asyncData ({ params, payload }) {
    const id = params.id // When calling /abc the slug will be "abc"
    if (payload) {
      console.log('payload', payload)
    } else {
      console.log('no payload', payload)
    }
    const something = payload ? payload.name : ''
    return { id, something }
  }
}
</script>
