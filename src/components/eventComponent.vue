<template>
  <div class="event-list">
    <h1>EVENT name </h1>
    <div :key="event.id" v-for="event of events">
      <EventItem :event="event"/>
    </div>
  </div>
</template>

<script>
import EventItem from "./eventItem.vue";

export default {
  name: "EventList",
  components: {
    EventItem
  },
  data() {
    return {
      events: {}
    };
  },
  created: function() {
    this.fetchData();
  },
  methods: {
    fetchData: async function() {
      try {
        const res = await fetch(
          "https://api.github.com/users/sdiachenko/events"
        );
        const json = await res.json();
        console.log(json);
        this.events = json;
      } catch (e) {
        console.log(e);
      }
    }
  },
  props: {
    name: String
  }
};
</script>

<style scoped>
.cont {
  border: black solid;
  background-color: beige;
}
</style>
