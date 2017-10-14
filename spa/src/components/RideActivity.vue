<template>
  <div class="ride-activity">
    <h5>{{ activity.name }}</h5>
    <span>{{ activity.time }}</span>
    <h4>{{ activity.title }}</h4>
    <div class="meta">
      <span><strong>{{ activity.distance }}km</strong></span>
      <span>{{ activity.elevation_gain }}m</span>
      <span>{{ activity.trophies }} trophies</span>
    </div>
    <button @click="addLike">{{ likes }} Likes</button>
    <button @click="toggleComments">{{ comments.length }} Comments</button>
    <div class="comments" v-show="show_comments">
      <p v-for="comment in comments"><i>{{ comment }}</i></p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RideActivity',
  props: [
    'activity'
  ],
  data () {
    return {
      likes: this.activity.likes,
      comments: this.activity.comments,
      show_comments: false
    }
  },
  methods: {
    addLike: function () {
      this.likes += 1
    },
    toggleComments: function () {
      this.show_comments = !this.show_comments
    }
  },
  components: {
  },
  mounted () {
  }
}
</script>

<style>
  .ride-activity {
    margin: 2em;
    padding: 0.5em;
    background-color: #EEE;
    border-radius: 5px;
  }
</style>
