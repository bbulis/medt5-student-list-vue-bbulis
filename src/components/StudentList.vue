<template>
  <ul class="collection with-header">
    <li class="collection-header"><h4>Schüler</h4></li>
    <StudentEntry
      v-for="student in this.students"
      v-bind:key="student.id"
      :student="student"
      v-on="$listeners"
    />
  </ul>
</template>

<script>
import StudentEntry from "@/components/StudentEntry";
export default {
  name: "StudentList",
  props: {
    students: Array,
  },
  components: {
    StudentEntry,
  },
};
</script>

<style scoped>

</style>