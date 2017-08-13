<template>
  <div class="footer">
    <v-footer :absolute="footer.fixed">
        <span>© {{ new Date().getFullYear() }}</span>
    </v-footer>
  </div>
</template>

<script>
  export default {
    data: () => ({
      footer: {
        fixed: false
      }
    })
  }
</script>


<style scoped>
  .footer {
    position: absolute;
    bottom: 0;
    width: 100%
  }
</style>
