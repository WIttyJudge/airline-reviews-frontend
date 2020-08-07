<template>
  <main class="mt-10">
    <div class="container mx-auto">
      <div class="mb-8 text-center">
        <h1 class="mb-4 text-3xl font-bold">AirlinesReview</h1>
        <p class="">Share your personam experience of any airline</p>
      </div>

      <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
        <AirlineCompanyCard/>
        <AirlineCompanyCard/>
        <AirlineCompanyCard/>
        <AirlineCompanyCard/>
        <AirlineCompanyCard/>

      </div>
    </div>
  </main>
</template>

<script>
import AirlineCompanyCard from '@/components/AirlineCompanyCard';

export default {
  name: "Home",

  components: {
    AirlineCompanyCard
  },
};
</script>
