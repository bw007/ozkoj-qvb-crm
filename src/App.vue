<template>
  <div class="page">
    <Sidebar />
    
  </div>
</template>
<script>
import Sidebar from './components/Sidebar.vue'
export default {
  components: {
    Sidebar,
  },
  data() {
    return {
      a: "Salom"
    }
  },
}
</script>
<style>
  body {
    background: #b1b1b1;
  }
</style>