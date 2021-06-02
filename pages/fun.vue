<template>
  <div>
    <span>This is fun</span>
    <v-btn to="/page"> To page page pls</v-btn>
    <h1>I am rendered on the {{ renderedOn }} side</h1>
  </div>
</template>


<script>
  export default {
    layout: 'layoutnew',
    // page component definitions
    asyncData() {
      return { renderedOn: process.client ? 'client' : 'server' }
    }
  }
</script>