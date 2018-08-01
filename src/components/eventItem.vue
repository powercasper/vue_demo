<template>
  <div class="event-item">
    <h2>{{event.type}}</h2>
    <p>ID: {{event.id}}</p>
    <p>Repo: {{event.repo.name}}</p>
  </div>
</template>

<script>
export default {
  name: "EventItem",
  props: ["event"]
};
</script>

<style scoped>
.event-item {
  background: yellow;
}
</style>
