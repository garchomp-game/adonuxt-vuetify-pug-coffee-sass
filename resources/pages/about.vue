<template lang="pug">
  h1 {{ params.name }}
</template>
<script lang="coffee">
querystring = require('querystring')
export default
  name: 'about'
  asyncData:(context) -> { params: querystring.parse(context.req._parsedUrl.query) }
</script>
<style lang="scss" scoped>
</style>
