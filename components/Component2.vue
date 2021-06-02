<template>
  <ol>
      <li>{{ groceryList.text }}</li>
   
  </ol>
</template>

<script>
export default {
     props: ['todo'],
   data() { return{
    groceryList: [
      { id: 0, text: 'Vegetables' },
      { id: 1, text: 'Cheese' },
      { id: 2, text: 'Whatever else humans are supposed to eat' }
    ]
    }
  }
}
</script>
