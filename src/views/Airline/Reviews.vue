<template>
<main class="container mx-auto">
  <h1>{{ slug }}</h1>
  <h1>{{ airline.averageScore }}</h1>
</main>
</template>

<script>
import gql from 'graphql-tag';

export default {
  props: ['slug'],

  apollo: {
    airline: gql`
      query {
        airline(slug: "third-airline") {
          name
          averageScore
        }
      }`
  }
}
</script>