<template>
  <div class="calendar-day" @click="setActiveDay(day.id)">
    <div class="header">{{day.abbvTitle}}</div>
    <div class="content">
      <CalendarEvent v-for="(event,index) in day.events" :key="index" :event="event"></CalendarEvent>
    </div>
  </div>
</template>
<script>
import { store } from "../store.js";
import CalendarEvent from "./CalendarEvent";
export default {
  name: "CalendarDay",
  props: ["day"],
  methods: {
    setActiveDay(dayId) {
      store.state.seedData.map(day =>
        day.id === dayId ? (day.active = true) : (day.active = false)
      );
    }
  },
  components: { CalendarEvent }
};
</script>
<style>
.calendar-day {
  width: 230px;
  height: auto;
  margin: 2px;
}
.calendar-day .header {
  padding: 10px;
  text-align: center;
  background-color: #0e1726;
  color: #d2d6dd;
}
.calendar-day .content {
  background-color: #37455b;
  padding-top: 8px;
  padding-bottom: 8px;
  min-height: 100px;
}
</style>