<template>
  <div class="activities">
      <h2>Your last activities</h2>
      <ride-activity v-for="activity in activities" :activity="activity"></ride-activity>
  </div>
</template>

<script>
import RideActivity from '@/components/RideActivity'

export default {
  name: 'Activities',
  props: {
  },
  data () {
    return {
      activities: [
        {
          name: 'Dyno Rider',
          title: 'Radfahrt am Nachmittag',
          time: 'Heute um 18:01',
          distance: 121.1,
          elevation_gain: 458,
          trophies: 17,
          likes: 3,
          comments: []
        },
        {
          name: 'Dyno Rider',
          title: 'Radfahrt am Vormittag (Pendeln)',
          time: 'Gestern um 08:43',
          distance: 4.9,
          elevation_gain: 21,
          trophies: 2,
          likes: 12,
          comments: ['Super, weiter so!', 'Krasses Wetter, oder?']
        }
      ]
    }
  },
  methods: {
  },
  components: {
    RideActivity
  },
  mounted () {
  }
}
</script>

<style>
</style>
