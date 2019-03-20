<template>
  <div class="calendar-week">
    <CalendarDay v-for="day in sharedState.seedData" :key="day.id" :day="day"></CalendarDay>
  </div>
</template>
<script>
import { store } from "../store.js";
import CalendarDay from "./CalendarDay.vue";
export default {
  name: "CalendarWeek",
  components: {
    CalendarDay
  },
  data() {
    return {
      sharedState: store.state
    };
  }
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
}
.calendar-week {
  display: grid;
  grid-template-columns: 230px 230px 230px 230px;
  grid-column-gap: 4px;
}
</style>