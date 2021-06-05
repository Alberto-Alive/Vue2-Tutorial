<template>
  <h1 class="red green--text">Hello World</h1>
</template>

<script>
  export default {
   head: {
    title: 'Home page',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Home page description'
      }
    ],
  },
loading:true,


transition(to, from) {
    if (!from) {
      return 'slide-left'
    }
    return +to.query.page < +from.query.page ? 'slide-right' : 'slide-left'
  }

  
  }
</script>

