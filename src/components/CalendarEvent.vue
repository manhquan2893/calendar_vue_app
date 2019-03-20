<template>
  <div class="calendar-event">{{event.details}}</div>
</template>
<script>
export default {
  name: "CalendarEvent",
  props: ["event"]
};
</script>
<style>
.calendar-event {
  width: 150px;
  min-height: 40px;
  margin: 8px auto;
  background-color: orangered;
  border-radius: 5px;
  color: black;
  display: flex;
  justify-content: center;
  align-items: center;
}
.calendar-event:first-child {
  margin-top: 0;
}
.calendar-event:last-child {
  margin-bottom: 0;
}
</style>