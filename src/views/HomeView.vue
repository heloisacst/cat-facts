<template>
  <div class="home">
    <Facts/>
  </div>
</template>

<script>
// @ is an alias to /src
import Facts from '@/components/Facts.vue'

export default {
  name: 'HomeView',
  components: {
    Facts
  }
}
</script>
