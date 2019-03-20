<template>
  <div class="calendar-entry">
    <div class="header">
      <input type="text" placeholder="New Event" v-model="entryText">
    </div>
    <div class="content">
      <span class="green-text">Day of Event:{{titleOfActiveDay}}</span>
    </div>
    <div>
      <button class="submit green-text" @click="submitEvent(entryText)">Submit</button>
    </div>
  </div>
</template>

<script>
import { store } from "../store.js";
export default {
  name: "CalendarEntry",
  data() {
    return {
      entryText: ""
    };
  },
  computed: {
    titleOfActiveDay() {
      return store.state.seedData.find(day => day.active).fullTitle;
    }
  },
  methods: {
    submitEvent(entryText) {
      store.state.seedData
        .find(day => day.active)
        .events.push({ details: entryText, edit: false });
      console.log(store.state.seedData.find(day => day.active).events);
    }
  }
};
</script>
<style>
.calendar-entry {
  width: 220px;
  margin: auto;
  margin-top: 100px;
}
.calendar-entry .header {
  border-bottom: gray 1px solid;
  padding: 6px;
}
.calendar-entry .header input {
  border: 0;
  padding: 5px;
}
.calendar-entry .content {
  padding: 10px 5px;
}
.calendar-entry button {
  background-color: transparent;
  border: green 1px solid;
  padding: 3px;
  cursor: pointer;
}
.green-text {
  color: green;
}
</style>
