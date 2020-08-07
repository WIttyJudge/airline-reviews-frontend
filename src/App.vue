<template>
  <div id="app">
    <NavbarLayout/>
    <router-view />
  </div>
</template>

<script>
import NavbarLayout from '@/layouts/NavbarLayout';

export default {
  components: {
    NavbarLayout
  }
}
</script>
