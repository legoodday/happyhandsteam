
<template>
  <main>
    <h1>快樂手，您的好朋友</h1>
  </main>
</template>

<script>
import { onMounted } from 'vue'

export default {
  setup() {
    onMounted(() => {
    document.title = '快樂手，您的好朋友'
      document.querySelector('meta[name="description"]')?.setAttribute('content', '快樂手，您的好朋友')
    })
  }
}

</script>
