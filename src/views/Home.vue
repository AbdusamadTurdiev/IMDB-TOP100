<template>
  <MoviesTable :items="movies" />
</template>

<script>
export default {
  name: 'Home',
  components: {
    MoviesTable: () => import('@/components/MoviesTable'),
  },
  computed: {
    movies() {
      return this.$store.getters.movies
    },
  },
}
</script>
