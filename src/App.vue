<script>
import { defineComponent } from 'vue'

import { RouterLink, RouterView } from 'vue-router'

export default defineComponent({
  components: {
    RouterLink,
    RouterView
  }
})
</script>

<template lang="pug">
  header
    nav.ui.fixed.top.menu
      RouterLink.item(to="/") Home
      RouterLink.item(to="/action") 連署護海岸

  .ui.container.main
    RouterView
</template>

<style scoped>
.main {
  margin-top: 100px;
}

.item.router-link-active {
  color: #000;
  background-color: #0f0;
}
</style>
