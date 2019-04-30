<template>
  <VContainer>
    <FullCalendar
      default-view="resourceTimeGridDay"
      :plugins="calendarPlugins"
      :events="events"
      :resources="resources"
    />
  </VContainer>
</template>

<script>
import FullCalendar from "@fullcalendar/vue";
import resourceTimeGridPlugin from "@fullcalendar/resource-timegrid";
// import dayGridPlugin from "@fullcalendar/daygrid";
export default {
  name: "home",
  components: {
    FullCalendar
  },
  data() {
    return {
      calendarPlugins: [resourceTimeGridPlugin],
      events: [
        {
          resourceId: "a",
          title: "event 1",
          start: "2019-04-28",
          end: "2019-05-01"
        },
        {
          resourceId: "b",
          title: "event 3",
          start: "2019-04-30T12:00:00+00:00",
          end: "2019-05-01T06:00:00+00:00"
        },
        {
          resourceId: "c",
          title: "event 4",
          start: "2019-04-30T07:30:00+00:00",
          end: "2019-04-30T09:30:00+00:00"
        },
        {
          resourceId: "a",
          title: "event 2",
          start: "2019-04-30T09:00:00+00:00",
          end: "2019-04-30T14:00:00+00:00"
        },
        {
          resourceId: "a",
          title: "event 5",
          start: "2019-04-30T12:00:00+00:00",
          end: "2019-04-30T15:00:00+00:00"
        },
        {
          resourceId: "a",
          title: "event 6",
          start: "2019-04-30T12:00:00+00:00",
          end: "2019-04-30T13:00:00+00:00"
        }
      ],
      resources: [
        { id: "a", title: "Peter Parker" },
        { id: "b", title: "Harry Osborn" },
        { id: "c", title: "Mary Jane" }
      ]
    };
  }
};
</script>

<style lang="scss">
@import "~@fullcalendar/core/main.css";
@import "~@fullcalendar/timegrid/main.css";
@import "~@fullcalendar/daygrid/main.css";
</style>
