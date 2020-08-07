<template>
  <div class="bg-white shadow-lg rounded-lg overflow-hidden">
    <div class="px-4 py-2">
      <h2 class="text-gray-900 font-bold text-xl uppercase">Airline 1</h2>
      <p class="text-gray-600 text-sm mt-1">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi quos
        quidem sequi illum facere recusandae voluptatibus
      </p>
    </div>

    <img
      class="h-48 w-full object-cover mt-2"
      src="https://images.unsplash.com/photo-1532882191016-9133c6d82083?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=320&q=80"
      alt="Airline"
    />

    <div class="flex items-center justify-between px-4 py-2 bg-gray-900">
      <span class="text-gray-200 font-bold text-lg">
        <StarsRaiting :config="config" />
      </span>
      <button
        class="px-2 py-1 bg-gray-200 text-xs text-gray-900 font-semibold rounded uppercase"
      >
        View Reviews
      </button>
    </div>
  </div>
</template>

<script>
import StarsRaiting from '@/components/StarsRaiting';

export default {
  data() {
    return {
      config: {
        rating: 4,
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