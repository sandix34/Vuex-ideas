<template>
  <div class="mt-8">
    <h1 class="text-3xl ">Ideas</h1>
    <div>
      <draggable class="flex flex-wrap flex-col content-center h-48 " v-model="allIdeas" group="ideas">
        <Idea v-for="idea in allIdeas" :key="idea.id" :item="idea" />
      </draggable>
    </div>
    <div class="flex justify-around">
      <div>
        <h3 class="text-3xl">Courses</h3>
        <draggable v-model="courses" group="ideas">
          <Idea v-for="course in courses" :key="course.id" :item="course" />
        </draggable>
      </div>
      <div>
        <h3 class="text-3xl">Paper work</h3>
        <draggable class="ideas" v-model="paperWork" group="ideas">
          <Idea v-for="pw in paperWork" :key="pw.id" :item="pw" />
        </draggable>
      </div>
      <div>
        <h3 class="text-3xl">Appointments</h3>
        <draggable v-model="appointments" group="ideas">
          <Idea v-for="apt in appointments" :key="apt.id" :item="apt" />
        </draggable>
      </div>
    </div>
  </div>
</template>

<script>
import draggable from "vuedraggable";
import Idea from "@/components/Idea";

export default {
  components: {
    draggable,
    Idea
  },
  computed: {
    allIdeas: {
      get() {
        return this.$store.getters.allIdeas;
      },
      set(value) {
        this.$store.dispatch("saveIdeasOrdering", value);
      }
    },
    courses: {
      get() {
        return this.$store.getters.courses;
      },
      set(value) {
        this.$store.dispatch("saveCoursesOrdering", value);
      }
    },
    paperWork: {
      get() {
        return this.$store.getters.paperWork;
      },
      set(value) {
        this.$store.dispatch("savePaperWorkOrdering", value);
      }
    },
    appointments: {
      get() {
        return this.$store.getters.appointments;
      },
      set(value) {
        this.$store.dispatch("saveAppointmentsOrdering", value);
      }
    }
  }
};
</script>

