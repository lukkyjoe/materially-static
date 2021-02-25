<template>
  <h1>{{ id }}</h1>
</template>

<script>
export default {
  asyncData ({ params }) {
    const id = params.id // When calling /abc the id will be "abc"
    return { id }
  }
}
</script>
