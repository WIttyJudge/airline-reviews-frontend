<template>
  <main class="mt-10">
    <div class="container mx-auto">
      <div class="mb-8 text-center">
        <h1 class="mb-4 text-3xl font-bold">AirlinesReview</h1>
        <p class="">Share your personal experience of any airline</p>
      </div>

      <section class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
        <div v-for="airline in airlines" :key="airline.id">
          <AirlineCompanyCard :airline="airline"/>
        </div>
      </section>

    </div>
  </main>
</template>

<script>
import gql from 'graphql-tag';

import AirlineCompanyCard from '@/components/AirlineCompanyCard';

export default {
  name: "Home",

  apollo: {
    airlines: gql`query {
      airlines{
        name
        imageUrl
        slug
        averageScore
      }
    }`
  },

  components: {
    AirlineCompanyCard
  },
};
</script>
