<template>
  <div class="bg-white shadow-lg rounded-lg overflow-hidden">
    <div class="px-4 py-2">
      <h2 class="text-gray-900 font-bold text-xl uppercase">{{ airline.name }}</h2>
      <p class="text-gray-600 text-sm mt-1">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi quos
        quidem sequi illum facere recusandae voluptatibus
      </p>
    </div>

    <img
      class="h-48 w-full object-cover mt-2"
      :src="airline.imageUrl"
      alt="Airline"
    />

    <div class="flex items-center justify-between px-4 py-2 bg-gray-800">
      <span class="text-gray-200 font-bold text-lg">
        <StarsRaiting :config="config" />
      </span>

      <router-link
        class="px-2 py-1 bg-gray-200 text-xs text-gray-900 font-semibold rounded uppercase"
        :to="{name: 'airlines#reviews', params: {slug: airline.slug}}"
      >
        View Reviews
      </router-link>

    </div>
  </div>
</template>

<script>
import StarsRaiting from '@/components/StarsRaiting';

export default {
  props: {
    airline: {
      type: Object, 
      required: true
    }
  },

  data() {
    return {
      config: {
        rating: this.airline.averageScore,
        isIndicatorActive: true,
        style: {
          fullStarColor: "#ed8a19",
          emptyStarColor: "#737373",
          starWidth: 20,
          starHeight: 20
        }
      }
    };
  },

  components: {
    StarsRaiting
  },
}
</script>