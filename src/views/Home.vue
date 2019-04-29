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
          end: "2019-04-30"
        },
        {
          resourceId: "b",
          title: "event 3",
          start: "2019-04-29T12:00:00+00:00",
          end: "2019-04-30T06:00:00+00:00"
        },
        {
          resourceId: "c",
          title: "event 4",
          start: "2019-04-29T07:30:00+00:00",
          end: "2019-04-29T09:30:00+00:00"
        },
        {
          resourceId: "d",
          title: "event 5",
          start: "2019-04-29T10:00:00+00:00",
          end: "2019-04-29T15:00:00+00:00"
        },
        {
          resourceId: "a",
          title: "event 2",
          start: "2019-04-29T09:00:00+00:00",
          end: "2019-04-29T14:00:00+00:00"
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
