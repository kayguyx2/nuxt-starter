<template>
  <div>
    <h1 class="text-3xl">Index page</h1>
    <div v-if="show">Show</div>
  </div>
</template>

<script>
export default {
  middleware: 'auth',
  data() {
    return {
      show: true
    }
  }
}
</script>