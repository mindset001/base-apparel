<template>
  <div class="home">
    <landing></landing>
  </div>
</template>

<script>
// @ is an alias to /src
import landing from '@/components/landing.vue'

export default {
  name: 'Home',
  components: {
    landing
  }
}
</script>
