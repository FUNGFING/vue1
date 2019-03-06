<template>
  <div class="home">
<news/>

  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import news from '@/components/news.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    news,

  },
  
}
</script>
