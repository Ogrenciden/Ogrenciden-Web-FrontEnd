<template>
  <div class="home">

<ad></ad>
<skeleton-loader v-if="loading" ></skeleton-loader>
  </div>
</template>

<script>
import ad from '@/components/ad.vue'
import skeletonLoader from '@/components/skeleton-loader.vue'
export default {
  components: {
    ad,
    skeletonLoader,
  },

  data() {
    return {
        loading: false,
    };
  },

  
}
</script>
