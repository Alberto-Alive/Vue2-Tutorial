<template>
    <div>

<span> Span is used for writing a line. This page will be found if you type /page in the url</span>
<NuxtLink type="button" to="/fun"><v-button> This is a big button</v-button></NuxtLink> 
<!-- //his shoud appear as a button.. -->

<!-- //it appears that we don't need the NuxtLink.. -->

<div><v-btn to="/fun"> To fun page pls</v-btn></div>


<NuxtLink to="/">Home page</NuxtLink> 
<!-- //let's see how this looks like; this will take you to the main page because it has "/" -->



</div>
</template>
<script>

export default {
     transition: 'page'
}
</script>

<style scoped>
.my-custom-active-link {
  color: green;
}
.home-enter-active, .home-leave-active { transition: opacity .5s; }
  .home-enter, .home-leave-active { opacity: 0; }
</style>